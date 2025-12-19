# AambaDB - Restaurant Analytics & Anomaly Detection System

![AambaDB Logo](https://img.shields.io/badge/AambaDB-Restaurant%20Analytics-blue?style=for-the-badge)
![Version](https://img.shields.io/badge/version-1.0.0-green?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-yellow?style=flat-square)

## 🚀 Project Overview

**AambaDB** is a comprehensive restaurant analytics and anomaly detection system designed to help restaurant owners and managers monitor, analyze, and optimize their business operations. The system leverages advanced machine learning algorithms, vector databases, and interactive dashboards to provide real-time insights into restaurant performance, detect anomalies in sales patterns, and generate detailed analytical reports.

### 🎯 Problem Statement

Modern restaurants generate vast amounts of data from POS systems, sales transactions, inventory, and customer interactions. However, most establishments lack the tools to:

- **Detect anomalies** in sales patterns, pricing, or inventory
- **Analyze trends** and predict future performance
- **Generate insights** from unstructured data
- **Monitor staff performance** and identify irregularities
- **Create comprehensive reports** for decision-making

AambaDB addresses these challenges by providing an AI-powered analytics platform that transforms raw restaurant data into actionable insights.

## ✨ Key Features

### 🔍 **Anomaly Detection Engine**
- **Real-time monitoring** of sales transactions, pricing, and staff behavior
- **Machine learning algorithms** to detect unusual patterns
- **Risk scoring system** for prioritizing anomalies
- **Automated alerts** for critical issues

### 📊 **Advanced Analytics Dashboard**
- **Interactive visualizations** with multiple chart types (bar, line, pie, area, heatmap)
- **Revenue tracking** and performance metrics
- **Staff performance monitoring** and history tracking
- **Calendar integration** for event-based analysis

### 🤖 **AI-Powered Query System**
- **Natural language processing** for data queries
- **Vector database integration** using FAISS
- **LangChain-powered** retrieval and analysis
- **Automated graph generation** based on queries

### 📱 **Cross-Platform Support**
- **Web dashboard** built with Next.js and React
- **Mobile application** developed with Flutter
- **Responsive design** for all screen sizes
- **Real-time data synchronization**

### 📄 **Intelligent Reporting**
- **PDF report generation** with custom branding
- **Email integration** for automated report delivery
- **Data export capabilities** in multiple formats
- **Scheduled reporting** functionality

### 🔐 **Security & Authentication**
- **Firebase authentication** with secure user management
- **Role-based access control** for different user types
- **Data encryption** and secure file handling
- **Session management** and token-based authentication

## 🛠️ Technology Stack

### **Frontend (Web Dashboard)**
- **Framework**: Next.js 15.2.4 with React 18
- **Styling**: Tailwind CSS with custom animations
- **UI Components**: Radix UI primitives
- **Charts**: Recharts for data visualization
- **State Management**: React hooks and context
- **Authentication**: Firebase Auth
- **Deployment**: Vercel-ready

### **Backend (API Server)**
- **Framework**: Flask with CORS support
- **AI/ML**: OpenAI GPT models, LangChain, FAISS vector store
- **Data Processing**: Pandas, NumPy, Matplotlib, Seaborn
- **File Handling**: PyPDF2, CSV parsing with encoding detection
- **Email**: SMTP integration for report delivery
- **PDF Generation**: ReportLab for custom reports

### **Mobile Application**
- **Framework**: Flutter
- **Platforms**: iOS, Android, Web, Desktop (Windows, macOS, Linux)
- **State Management**: Provider/Bloc pattern
- **Authentication**: Firebase integration
- **Platform Features**: Native device integration

### **Database & Storage**
- **Primary Database**: Firebase Firestore
- **Vector Database**: FAISS for similarity search
- **File Storage**: Firebase Storage
- **Local Storage**: Browser localStorage for session data

### **DevOps & Tools**
- **Version Control**: Git with GitHub
- **Package Management**: npm/pnpm (Frontend), pip (Backend), pub (Flutter)
- **Build Tools**: Next.js build system, Gradle (Android), Xcode (iOS)
- **Environment Management**: dotenv for configuration

## 🏗️ Project Architecture

```
AambaDB/
├── 📁 App/                          # Mobile Application
│   ├── 📁 android/                  # Android-specific files
│   ├── 📁 ios/                      # iOS-specific files
│   ├── 📁 fin_anominal_again/       # Flutter app source
│   ├── 📁 linux/                    # Linux desktop support
│   ├── 📁 macos/                    # macOS desktop support
│   └── 📁 windows/                  # Windows desktop support
│
├── 📁 restaurant-dashboard/         # Web Dashboard (Next.js)
│   ├── 📁 app/                      # App router pages
│   │   ├── 📁 (dashboard)/          # Dashboard routes
│   │   │   ├── 📁 analytics/        # Analytics page
│   │   │   ├── 📁 anomalies/        # Anomaly detection
│   │   │   ├── 📁 upload-sales/     # Data upload interface
│   │   │   └── 📁 dashboard/        # Main dashboard
│   │   ├── 📁 api/                  # API routes
│   │   └── 📁 login/                # Authentication
│   ├── 📁 components/               # Reusable UI components
│   │   ├── 📁 charts/               # Chart components
│   │   └── 📁 ui/                   # Base UI components
│   └── 📁 lib/                      # Utility functions
│
├── 📁 restro-Backend/               # Python Flask API
│   └── rag.py                       # Main backend logic
│
├── 📁 Frontend-vectdb/              # Vector Database Storage
│   ├── 📁 graphs/                   # Generated visualizations
│   └── 📁 vectordb/                 # FAISS vector store
│
└── 📁 uploads/                      # File upload directory
```

## 🚀 Installation & Setup

### Prerequisites

- **Node.js** 18+ and npm/pnpm
- **Python** 3.8+ with pip
- **Flutter** SDK 3.0+
- **Firebase** project with Firestore and Auth enabled
- **OpenAI API** key for AI functionality

### 1. Clone the Repository

```bash
git clone https://github.com/Nair-Abhinav/codeshastraxi_AambaDB.git
cd codeshastraxi_AambaDB
```

### 2. Backend Setup (Flask API)

```bash
cd restro-Backend

# Install Python dependencies
pip install -r requirements.txt

# Create environment file
echo "OPENAI_API_KEY=your_openai_api_key_here" > .env
echo "EMAIL_HOST=smtp.gmail.com" >> .env
echo "EMAIL_PORT=587" >> .env
echo "EMAIL_USER=your_email@gmail.com" >> .env
echo "EMAIL_PASSWORD=your_app_password" >> .env

# Start the Flask server
python rag.py
```

The backend will run on `http://localhost:5000`

### 3. Frontend Setup (Next.js Dashboard)

```bash
cd restaurant-dashboard

# Install dependencies
pnpm install

# Create environment file
cat > .env.local << EOF
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
EOF

# Start development server
pnpm dev
```

The frontend will run on `http://localhost:3000`

### 4. Mobile App Setup (Flutter)

```bash
cd App/fin_anominal_again

# Get Flutter dependencies
flutter pub get

# Run on desired platform
flutter run                    # Default platform
flutter run -d chrome         # Web
flutter run -d windows        # Windows
flutter run -d android        # Android (with device/emulator)
flutter run -d ios           # iOS (macOS only)
```

## 📱 Usage Guide

### 1. **Data Upload & Processing**

1. Navigate to the **Upload Sales** section in the dashboard
2. Upload CSV or PDF files containing restaurant data
3. The system automatically processes and creates a vector database
4. Data is analyzed for patterns and potential anomalies

### 2. **Anomaly Detection**

1. Visit the **Anomalies** page to view detected issues
2. Review anomalies by risk score (High, Medium, Low)
3. Filter by date range, staff member, or category
4. Take action on flagged transactions

### 3. **Analytics Dashboard**

1. Monitor key metrics on the main dashboard:
   - Daily orders and revenue
   - Staff performance metrics
   - Peak hours analysis
   - Trend visualizations

### 4. **AI-Powered Queries**

1. Use natural language to query your data:
   - "Show me sales trends for last month"
   - "Which staff member has the highest returns?"
   - "Generate a report on weekend performance"

### 5. **Report Generation**

1. Generate automated PDF reports
2. Schedule email delivery to stakeholders
3. Export data in various formats
4. Customize report templates

## 🔌 API Documentation

### Core Endpoints

#### `POST /query`
Process natural language queries and generate insights
```json
{
  "query": "Show me revenue trends for the last 30 days",
  "email": "user@restaurant.com"
}
```

#### `POST /process_file`
Upload and process restaurant data files
```json
{
  "file": "multipart/form-data",
  "file_type": "csv|pdf"
}
```

#### `POST /download_report`
Generate and download PDF reports
```json
{
  "query": "Monthly performance report",
  "response": "Generated analysis",
  "include_graphs": true
}
```

#### `GET /graph/<graph_id>`
Retrieve generated visualization by ID

#### `POST /diagnose`
Run comprehensive system diagnostics

### Authentication
All endpoints support Firebase token-based authentication. Include the token in the Authorization header:
```
Authorization: Bearer <firebase_id_token>
```

## 🔍 Key Features in Detail

### **Anomaly Detection Algorithm**
- **Statistical Analysis**: Z-score and IQR-based outlier detection
- **Machine Learning**: Isolation Forest for complex pattern recognition
- **Time-series Analysis**: Seasonal decomposition for trend analysis
- **Risk Scoring**: Weighted scoring based on multiple factors

### **Vector Database Integration**
- **FAISS Storage**: Efficient similarity search for large datasets
- **Embedding Generation**: OpenAI embeddings for semantic search
- **Query Processing**: LangChain for intelligent data retrieval
- **Real-time Updates**: Incremental updates to vector store

### **Visualization Engine**
- **Dynamic Charts**: Automatic chart type selection based on data
- **Interactive Elements**: Zoom, filter, and drill-down capabilities
- **Export Options**: PNG, PDF, and SVG export formats
- **Responsive Design**: Mobile-optimized visualizations

## 🧪 Testing

### Backend Testing
```bash
cd restro-Backend
python -m pytest tests/
```

### Frontend Testing
```bash
cd restaurant-dashboard
pnpm test
```

### Flutter Testing
```bash
cd App/fin_anominal_again
flutter test
```

## 🚀 Deployment

### Production Deployment

#### Backend (Flask API)
```bash
# Using Gunicorn
pip install gunicorn
gunicorn -w 4 -b 0.0.0.0:5000 rag:app
```

#### Frontend (Next.js)
```bash
cd restaurant-dashboard
pnpm build
pnpm start
```

#### Mobile App
```bash
# Android
flutter build apk --release

# iOS
flutter build ios --release

# Web
flutter build web
```

### Docker Deployment
```dockerfile
# Backend Dockerfile
FROM python:3.9
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["python", "rag.py"]
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🎥 Demo & Documentation

### 📹 **Video Demonstration**
🎬 **[Watch Project Demo Video](https://drive.google.com/file/d/1-grJpwME78HN3jAvIs3xVybdHtEVVFYs/view?usp=sharing)**

*Click the link above to view a comprehensive demonstration of Projects's features, including the anomaly detection system, analytics dashboard, AI-powered queries, and report generation capabilities.*

## 👥 Team
- **Vedant Kesharia** - Full Stack Developer and AI Researcher
- **Rohit Rai** - Developer
- **Krishna Naudiyal** - Developer
- **Abhinav Nair** - Full-stack Developer

<div align="center">
  <p><strong>Built with ❤️ for the restaurant industry</strong></p>
  <p>
    <a href="#-project-overview">Overview</a> •
    <a href="#-key-features">Features</a> •
    <a href="#-installation--setup">Setup</a> •
    <a href="#-usage-guide">Usage</a> •
    <a href="#-api-documentation">API</a>
  </p>
</div>
