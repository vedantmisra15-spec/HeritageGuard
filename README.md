# HeritageGuard: AI for Cultural Preservation & Sustainable Tourism

![HeritageGuard Banner](https://img.shields.io/badge/Project-HeritageGuard-8B4513?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Prototype-DAA520?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-3.0.0-black?style=for-the-badge&logo=flask)

## 📋 Project Overview

**HeritageGuard** is an AI-powered system designed to preserve cultural heritage sites through intelligent prediction, restoration, and authenticity verification. This academic project demonstrates the application of Machine Learning, Computer Vision, and Natural Language Processing in sustainable tourism management.

### 🎯 Key Objectives

1. **Predictive Analytics**: Forecast tourist crowd levels to prevent site degradation
2. **Digital Restoration**: Restore damaged historical artifacts using AI
3. **Authenticity Verification**: Detect cultural authenticity in tourism content
4. **Sustainable Tourism**: Balance preservation with economic benefits
5. **Environmental Monitoring**: Track risks to heritage sites
6. **Knowledge Sharing**: Platform for heritage managers worldwide

## 🏗️ Architecture

### Tech Stack

**Frontend:**
- HTML5, CSS3, JavaScript (ES6+)
- Chart.js for data visualization
- Responsive design with CSS Grid and Flexbox
- Modern UI with heritage-inspired aesthetics

**Backend:**
- Python 3.8+
- Flask 3.0.0 (REST API framework)
- Flask-CORS for cross-origin support
- Mock AI implementations (for prototype demonstration)

### System Components

```
HeritageGuard/
├── Frontend/
│   ├── index.html         # Landing page
│   ├── dashboard.html     # Analytics dashboard
│   ├── styles.css         # Comprehensive styling
│   ├── script.js          # Landing page interactions
│   └── dashboard.js       # Dashboard API integration
│
├── Backend/
│   ├── app.py            # Flask API server
│   └── requirements.txt  # Python dependencies
│
└── README.md             # This file
```

## 🚀 Installation & Setup

### Prerequisites

- Python 3.8 or higher
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Basic understanding of REST APIs

### Step 1: Clone or Download the Project

```bash
# If using git
git clone <repository-url>
cd HeritageGuard

# Or simply extract the ZIP file to a folder
```

### Step 2: Set Up Backend (Python/Flask)

1. **Navigate to the project directory:**
   ```bash
   cd HeritageGuard
   ```

2. **Install Python dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
   
   Or install manually:
   ```bash
   pip install Flask==3.0.0 flask-cors==4.0.0
   ```

3. **Run the Flask server:**
   ```bash
   python app.py
   ```

4. **Verify backend is running:**
   - You should see output: `Server running on http://localhost:5000`
   - Open browser and visit: `http://localhost:5000`
   - You should see API information in JSON format

### Step 3: Set Up Frontend

1. **Open the frontend in a browser:**
   
   **Option A: Using Python HTTP Server (Recommended)**
   ```bash
   # In a NEW terminal window (keep Flask running in the first)
   python -m http.server 8000
   ```
   Then open: `http://localhost:8000`

   **Option B: Using Live Server (VS Code)**
   - Install "Live Server" extension in VS Code
   - Right-click on `index.html`
   - Select "Open with Live Server"

   **Option C: Direct File Access**
   - Simply open `index.html` in your browser
   - Note: Some browsers may restrict API calls with file:// protocol

2. **Verify frontend is working:**
   - Landing page should load with heritage-themed design
   - Click "Launch Dashboard" to access the analytics interface

## 📊 API Endpoints

### 1. Crowd Prediction
**Endpoint:** `POST /api/predict-crowd`

**Request Body:**
```json
{
  "site_id": 1,
  "date": "2024-02-15"
}
```

**Response:**
```json
{
  "success": true,
  "site": {
    "id": 1,
    "name": "Taj Mahal",
    "location": "Agra, India"
  },
  "prediction": {
    "crowd_level": "Medium",
    "confidence": 87.5,
    "estimated_visitors": 3500,
    "recommendation": "Moderate crowds expected..."
  },
  "hourly_forecast": [...]
}
```

### 2. Image Restoration
**Endpoint:** `POST /api/restore-image`

**Request Body:**
```json
{
  "image_name": "artifact_001.jpg",
  "damage_type": "scratches"
}
```

**Response:**
```json
{
  "success": true,
  "restoration": {
    "quality_score": 92.5,
    "processing_time_seconds": 2.3,
    "damage_detected": "scratches",
    "ai_confidence": 94.2
  },
  "before_after_metrics": {
    "clarity_improvement": "+45%",
    "color_accuracy": "92%"
  }
}
```

### 3. Authenticity Check
**Endpoint:** `POST /api/check-authenticity`

**Request Body:**
```json
{
  "content": "Sample cultural content text...",
  "category": "product"
}
```

**Response:**
```json
{
  "success": true,
  "analysis": {
    "authenticity_score": 85.3,
    "authenticity_level": "Highly Authentic",
    "status_color": "green"
  },
  "nlp_metrics": {
    "cultural_accuracy": 88.5,
    "historical_correctness": 91.2
  },
  "red_flags": [],
  "recommendations": [...]
}
```

### 4. Dashboard Summary
**Endpoint:** `GET /api/dashboard-summary`

**Response:**
```json
{
  "success": true,
  "overview": {
    "total_sites_monitored": 4,
    "sites_at_risk": 1
  },
  "crowd_status": {
    "current_level": "Medium",
    "today_visitors": 5432
  },
  "environmental_risk": {
    "level": "Low"
  },
  "ai_performance": {...}
}
```

### 5. Heritage Sites List
**Endpoint:** `GET /api/heritage-sites`

### 6. Health Check
**Endpoint:** `GET /api/health`

## 🎨 Features Demonstration

### 1. Landing Page
- **Hero Section**: Overview of HeritageGuard mission
- **About Section**: Problems addressed by the system
- **Features Section**: Detailed explanation of AI capabilities
- **Impact Metrics**: Comparison with traditional methods
- **Objectives**: Project goals and vision

### 2. Dashboard
- **Overview Cards**: Real-time metrics display
  - Current crowd level
  - Sites monitored
  - Environmental risk
  - Authenticity score

- **AI Processing Modules**:
  - Crowd Prediction Module
  - Image Restoration Module
  - Authenticity Detection Module

- **Analytics Charts**:
  - Weekly visitor trends (Chart.js)
  - AI performance metrics

- **System Alerts**: Real-time notifications

## 🧪 Testing the System

### Test Scenario 1: Crowd Prediction
1. Open Dashboard
2. Select a heritage site (e.g., "Taj Mahal")
3. Choose a prediction date
4. Click "Predict Crowd Level"
5. Observe results showing crowd level, confidence, and recommendations

### Test Scenario 2: Image Restoration
1. Enter an artifact name (e.g., "heritage_photo_1947.jpg")
2. Select damage type (e.g., "Fading")
3. Click "Restore Image"
4. View restoration quality metrics and improvement statistics

### Test Scenario 3: Authenticity Check
1. Enter or modify cultural content text
2. Select content category
3. Click "Analyze Authenticity"
4. Review authenticity score, NLP metrics, and recommendations

## 🔧 Troubleshooting

### Backend Issues

**Problem**: `ModuleNotFoundError: No module named 'flask'`
**Solution**: Install Flask using `pip install Flask flask-cors`

**Problem**: Port 5000 already in use
**Solution**: 
```python
# In app.py, change the port:
app.run(debug=True, port=5001)

# Update API_BASE_URL in dashboard.js:
const API_BASE_URL = 'http://localhost:5001/api';
```

**Problem**: CORS errors in browser console
**Solution**: Ensure `flask-cors` is installed and CORS(app) is called in app.py

### Frontend Issues

**Problem**: API calls failing with "Failed to fetch"
**Solution**: 
1. Verify backend is running (`python app.py`)
2. Check backend URL in `dashboard.js` matches your setup
3. Open browser console (F12) to see detailed error messages

**Problem**: Charts not displaying
**Solution**: Ensure Chart.js CDN is accessible. Check browser console for errors.

**Problem**: Styles not loading correctly
**Solution**: Clear browser cache (Ctrl+Shift+Delete) and reload page

## 📚 Academic Usage

### For Presentations
- Use the landing page to introduce the project concept
- Navigate to dashboard for live demonstrations
- Show API responses in browser DevTools (F12 → Network tab)

### For Documentation
- Code is heavily commented for easy understanding
- Each function has clear purpose documentation
- RESTful API follows best practices

### For Viva/Defense
- Explain the mock AI logic in `app.py`
- Discuss how real ML models would replace mock functions
- Demonstrate understanding of:
  - REST API architecture
  - Frontend-backend communication
  - Asynchronous JavaScript (Promises/Async-Await)
  - Data visualization with Chart.js

## 🎓 Learning Outcomes

This project demonstrates understanding of:

1. **Full-Stack Development**: Frontend and backend integration
2. **RESTful APIs**: Designing and consuming REST endpoints
3. **Asynchronous Programming**: JavaScript Promises and Async/Await
4. **Data Visualization**: Using Chart.js for analytics
5. **Responsive Design**: Mobile-friendly UI using CSS Grid/Flexbox
6. **AI Concepts**: Understanding ML, CV, and NLP applications
7. **System Architecture**: Designing scalable web applications

## 🔮 Future Enhancements

To convert this prototype into a production system:

1. **Real AI Models**:
   - Implement actual ML models using TensorFlow/PyTorch
   - Train crowd prediction models on historical data
   - Integrate GANs for image restoration
   - Use BERT/GPT for NLP authenticity detection

2. **Database Integration**:
   - Add PostgreSQL/MongoDB for data persistence
   - Store user accounts and site data
   - Log predictions and restorations

3. **Authentication**:
   - Implement JWT-based authentication
   - Role-based access control (Admin, Manager, Viewer)

4. **Advanced Features**:
   - Real-time notifications with WebSockets
   - File upload for image restoration
   - Export reports as PDF
   - Multi-language support

5. **Deployment**:
   - Deploy backend to AWS/Heroku
   - Host frontend on Netlify/Vercel
   - Set up CI/CD pipeline

## 📞 Support

For academic support or questions about the project:
- Review inline code comments
- Check browser console for errors (F12)
- Verify backend is running on port 5000
- Ensure all dependencies are installed

## 📄 License

This is an academic project developed for educational purposes.

## 🙏 Acknowledgments

- UNESCO for heritage site data inspiration
- Chart.js for visualization library
- Flask community for excellent documentation
- Cultural preservation organizations worldwide

---

**Developed by**: [Your Name]  
**Course**: [Your Course]  
**Institution**: [Your Institution]  
**Date**: February 2024

**For Academic Use Only** - This is a prototype demonstration using mock AI implementations.
