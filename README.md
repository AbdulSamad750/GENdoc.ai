# GENdoc.ai
🚀 AI-powered document scanner using Azure AI &amp; OpenAI - Automatically classifies, organizes &amp; searches documents | Microsoft Imagine Cup 2026
# 🔧 DocuGenius Backend - AI Document Processing API

> Secure backend API powering AI-driven document intelligence

[![Node.js](https://img.shields.io/badge/Node.js-18.x-green)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.x-lightgrey)](https://expressjs.com/)
[![Azure AI](https://img.shields.io/badge/Azure-AI%20Services-0078d4)](https://azure.microsoft.com/)

## 📖 About

Backend API for DocuGenius that handles document processing, text extraction, and AI-powered classification. Integrates Azure AI Document Intelligence and OpenAI GPT-4o-mini to deliver intelligent document analysis.

## 🛠️ Tech Stack

- **Runtime**: Node.js 18+
- **Framework**: Express.js
- **AI Services**: 
  - Azure AI Document Intelligence (OCR)
  - OpenAI GPT-4o-mini (Classification)
- **File Handling**: Multer
- **Security**: CORS, Environment Variables
- **HTTP Client**: Axios

## ✨ Features

- 📄 **Document Processing** - Handles image and PDF uploads
- 🤖 **OCR Integration** - Azure AI Document Intelligence for text extraction
- 🧠 **AI Classification** - OpenAI GPT-4o-mini for intelligent categorization
- 🔒 **Secure** - API keys protected with environment variables
- ⚡ **Fast** - Efficient processing with async/await
- 🌐 **CORS Enabled** - Cross-origin requests supported

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager
- Azure AI Document Intelligence resource
- OpenAI API key

### Installation
```bash
# Clone the repository
git clone https://github.com/shaikhabdulsamad/docugenius-backend.git

# Navigate to project directory
cd docugenius-backend

# Install dependencies
npm install

# Create .env file
cp .env.example .env
```

### Environment Variables

Create a `.env` file in the root directory with your API keys:
```env
# Azure AI Document Intelligence
AZURE_DOC_INTELLIGENCE_KEY=your_azure_key_here
AZURE_DOC_INTELLIGENCE_ENDPOINT=https://your-resource.cognitiveservices.azure.com/

# OpenAI
OPENAI_API_KEY=your_openai_key_here

# Server
PORT=5000
```

**⚠️ IMPORTANT**: Never commit `.env` file to GitHub! It's already in `.gitignore`.

### Running Locally
```bash
# Start development server
node server.js

# Server will run on http://localhost:5000
```

## 📡 API Endpoints

### Health Check
```http
GET /api/health
```

**Response:**
```json
{
  "status": "OK",
  "message": "DocuGenius API is running!"
}
```

### Process Document
```http
POST /api/process-document
Content-Type: multipart/form-data
```

**Request:**
- `file`: Document file (image or PDF)

**Response:**
```json
{
  "success": true,
  "text": "Extracted text from document...",
  "analysis": {
    "type": "Bill",
    "category": "Financial",
    "keyInfo": {
      "date": "Dec 2025",
      "amount": "₹4,270",
      "vendor": "BEST Mumbai",
      "important": "Electricity bill"
    },
    "summary": "This is an electricity bill from BEST Mumbai",
    "tags": ["electricity", "bill", "financial"]
  }
}
```

## 🏗️ Project Structure
```
docugenius-backend/
├── server.js           # Main application file
├── .env               # Environment variables (DO NOT COMMIT)
├── .env.example       # Example environment file
├── .gitignore         # Git ignore file
├── package.json       # Dependencies
└── README.md          # This file
```

## 🔐 Security

- ✅ API keys stored in environment variables
- ✅ `.env` file excluded from Git
- ✅ CORS configured for security
- ✅ File size limits enforced (10MB max)
- ✅ File type validation (images and PDFs only)

## 📦 Dependencies
```json
{
  "express": "^4.18.2",
  "cors": "^2.8.5",
  "dotenv": "^16.3.1",
  "axios": "^1.6.0",
  "multer": "^1.4.5-lts.1",
  "form-data": "^4.0.0"
}
```

## 🚀 Deployment

### Deploy to Render

1. Push code to GitHub
2. Create new Web Service on Render
3. Connect your GitHub repository
4. Add environment variables in Render dashboard
5. Deploy!

**Build Command:**
```bash
npm install
```

**Start Command:**
```bash
node server.js
```

## 🧪 Testing

### Test Health Endpoint
```bash
curl http://localhost:5000/api/health
```

### Test Document Processing
```bash
curl -X POST http://localhost:5000/api/process-document \
  -F "file=@/path/to/document.jpg"
```

## ⚙️ Configuration

### Supported File Types
- Images: JPG, JPEG, PNG, GIF
- Documents: PDF

### File Size Limits
- Maximum: 10MB per file

### Processing Flow
1. Client uploads document
2. Multer handles file upload
3. Azure AI extracts text (OCR)
4. OpenAI classifies document
5. Structured data returned to client

## 🐛 Troubleshooting

### "401 Unauthorized" Error
- Check Azure AI key and endpoint in `.env`
- Verify keys are correct in Azure Portal

### "Module not found" Error
```bash
npm install
```

### "Port already in use" Error
```bash
# Change PORT in .env file
PORT=5001
```

## 🤝 Contributing

This project was built for Microsoft Imagine Cup 2026. Contributions welcome!

## 👨‍💻 Author

**Abdul Samad Shaikh**
- 🏫 M.H. Saboo Siddik College of Engineering, Mumbai
- 📧 Email: samad.221435.it@mhscce.ac.in
- 

## 🏆 Microsoft Imagine Cup 2026

Built for Microsoft Imagine Cup 2026 - Demonstrating cloud AI integration for real-world problems.

## 📄 License

Created for educational purposes as part of Microsoft Imagine Cup 2026.

## 🙏 Acknowledgments

- Microsoft Azure AI Services
- OpenAI API
- Express.js community
- Node.js team

---

⭐ **Star this repo if you found it helpful!**

🔗 **Related**: [Frontend Repository](https://github.com/shaikhabdulsamad/docugenius-frontend)
```

---

## 📝 **.gitignore FILE (VERY IMPORTANT!)**

### **For Frontend:**
```
# Dependencies
node_modules/

# Production
build/

# Environment variables
.env
.env.local
.env.production.local

# Misc
.DS_Store
npm-debug.log*
yarn-debug.log*
yarn-error.log*
```

### **For Backend:**
```
# Dependencies
node_modules/

# Environment variables
.env

# Logs
*.log
npm-debug.log*

# OS files
.DS_Store

# Usage stats
usage-stats.json
```

---

## 🏷️ **TOPICS/TAGS TO ADD**

When creating repositories, add these topics:

**Frontend:**
```
react, azure-ai, document-scanner, ai, openai, document-management, imagine-cup, microsoft, frontend, typescript
```

**Backend:**
```
nodejs, express, azure-ai, openai, api, backend, document-processing, imagine-cup, microsoft, rest-api
