# 🚀 Quick Start Guide - HeritageGuard

## ⚡ 3-Minute Setup

### Step 1: Install Backend Dependencies
```bash
pip install Flask==3.0.0 flask-cors==4.0.0
```

### Step 2: Start Backend Server
```bash
python app.py
```
✅ You should see: "Server running on http://localhost:5000"

### Step 3: Start Frontend
Open a NEW terminal (keep backend running):

```bash
python -m http.server 8000
```

### Step 4: Open in Browser
Visit: **http://localhost:8000**

---

## 🎯 Quick Test

1. Click "Launch Dashboard"
2. Try "Predict Crowd Level" - Select site and date, click predict
3. Try "Restore Image" - Click restore button
4. Try "Authenticity Check" - Click analyze button

---

## ⚠️ Common Issues

**Issue**: API not connecting
**Fix**: Make sure backend is running on port 5000

**Issue**: Module not found
**Fix**: `pip install Flask flask-cors`

**Issue**: Port 5000 busy
**Fix**: Kill the process or change port in app.py and dashboard.js

---

## 📁 Project Structure

```
HeritageGuard/
├── app.py              # Backend API
├── requirements.txt    # Python dependencies
├── index.html          # Landing page
├── dashboard.html      # Dashboard
├── styles.css          # All styles
├── script.js           # Landing page JS
├── dashboard.js        # Dashboard JS
└── README.md           # Full documentation
```

---

## 🎓 For Academic Presentation

1. **Introduction** - Use landing page (index.html)
2. **Features Demo** - Show dashboard functionality
3. **Technical Details** - Show code in app.py and dashboard.js
4. **Results** - Demonstrate API calls in browser DevTools (F12)

---

## 📊 API Testing

### Using Browser DevTools (F12)
1. Open Dashboard
2. Press F12 → Network tab
3. Click any AI module button
4. See API request/response in real-time

### Using cURL
```bash
# Test crowd prediction
curl -X POST http://localhost:5000/api/predict-crowd \
  -H "Content-Type: application/json" \
  -d '{"site_id": 1, "date": "2024-02-15"}'

# Test dashboard summary
curl http://localhost:5000/api/dashboard-summary
```

---

## 💡 Tips for Viva

- Explain that AI logic is mocked (using random.choice, etc.)
- Discuss how real ML models would replace mock functions
- Highlight REST API best practices (status codes, JSON, CORS)
- Show understanding of frontend-backend communication
- Demonstrate responsive design

---

## 🆘 Need Help?

1. Check if backend is running: `http://localhost:5000`
2. Open browser console (F12) to see errors
3. Verify Python version: `python --version` (need 3.8+)
4. Check README.md for detailed troubleshooting

---

**Ready to Present? You're all set! 🎉**
