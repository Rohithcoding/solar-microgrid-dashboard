<<<<<<< HEAD
# ☀️ Solar Microgrid Dashboard - SIH Demo

## 🎯 Overview

A complete IoT-based Solar Microgrid Monitoring System built with **Streamlit** for your SIH presentation. This system provides real-time monitoring, alert management, and data visualization for rural microgrids without requiring any hardware.

## ✨ Features

- 🔐 **Phone Authentication** - Secure operator login with OTP
- 📊 **Real-time Dashboard** - Live energy, battery, and weather monitoring
- 🚨 **Smart Alert System** - Professional notifications with 1-minute intervals
- 📈 **Interactive Charts** - Beautiful data visualizations with Plotly
- 📱 **Mobile Responsive** - Works perfectly on all devices
- 🎨 **Modern UI** - Glassmorphism effects and smooth animations
- ⚡ **No Hardware Required** - Complete software simulation

## 🚀 Quick Start

### Option 1: One-Command Deployment
```bash
./deploy-streamlit.sh
```

### Option 2: Manual Installation
```bash
# Install dependencies
pip3 install -r requirements-streamlit.txt

# Run the application
streamlit run deploy-streamlit.py
```

### Option 3: Single Command
```bash
pip3 install streamlit plotly pandas numpy && streamlit run deploy-streamlit.py
```

## 🌐 Access Dashboard

Once started, open your browser:
- **Local:** http://localhost:8501
- **Network:** http://your-ip:8501

## 🔑 Demo Credentials

- **Phone Number:** Any number (e.g., 9845280208)
- **OTP:** 123456

## 📱 Perfect for SIH Demo

### What Judges Will See:
1. **Professional Login** - Phone number authentication
2. **Real-time Dashboard** - Live data updates every 5 seconds
3. **Beautiful Charts** - Interactive energy monitoring
4. **Smart Alerts** - Professional notification system
5. **Mobile Responsive** - Works on any device
6. **No Hardware Required** - Pure software simulation

### Demo Flow:
1. Open http://localhost:8501
2. Login with any phone number + OTP: 123456
3. Show real-time dashboard with live data
4. Demonstrate interactive charts and metrics
5. Show alert system in action
6. Display mobile responsiveness

## 📁 Project Structure

```
sih-demo/
├── deploy-streamlit.py          # Main Streamlit application
├── deploy-streamlit.sh          # Deployment script
├── requirements-streamlit.txt   # Python dependencies
├── STREAMLIT_DEPLOYMENT.md     # Detailed documentation
└── README.md                   # This file
```

## 🛠️ Technical Details

### Dependencies
- **Streamlit** - Web application framework
- **Plotly** - Interactive charts and graphs
- **Pandas** - Data manipulation
- **NumPy** - Numerical computing

### Data Simulation
- **1000 data points** of historical energy and weather data
- **5-second intervals** for real-time simulation
- **Daily patterns** with realistic variations
- **No external APIs** required

### Alert System
- **Battery SOC:** Critical < 30%, Warning < 50%
- **Temperature:** Critical > 40°C, Warning > 35°C
- **Generation:** Warning < 1000W
- **Efficiency:** Warning < 75%
- **Smart timing:** 1-minute intervals

## 🎨 Customization

### Changing Alert Thresholds
Edit the `check_alerts()` function in `deploy-streamlit.py`:
```python
# Battery alerts
if energy_data['storage_soc_percent'] < 30:  # Change threshold
    # Critical alert logic
```

### Modifying Data Patterns
Edit the `generate_historical_data()` function:
```python
# Energy data patterns
generation = 1800 + 600 * np.sin(2 * np.pi * hours / 24) + np.random.normal(0, 100, 1000)
# Modify base values and patterns here
```

## 🚀 Deployment Options

### Local Development
```bash
streamlit run deploy-streamlit.py
```

### Production
```bash
streamlit run deploy-streamlit.py --server.port 8501 --server.address 0.0.0.0
```

### Cloud Deployment
- **Streamlit Cloud** - Upload to GitHub and deploy
- **Heroku** - Add Procfile and deploy
- **Railway** - Connect GitHub repository
- **AWS/GCP/Azure** - Use container services

## 📞 Support

For issues:
1. Check console output for errors
2. Ensure Python 3.7+ is installed
3. Verify all dependencies are installed
4. Check if port 8501 is available

## 🎉 Success!

Your Solar Microgrid Dashboard is ready for the SIH presentation!

**Key Benefits:**
- ✅ **Single file deployment** - Easy to share and run
- ✅ **No external dependencies** - Works offline
- ✅ **Professional appearance** - Impresses judges
- ✅ **Real-time simulation** - Shows live data
- ✅ **Mobile responsive** - Works on any device
- ✅ **Complete functionality** - All features included

**Demo URL:** http://localhost:8501  
**Demo OTP:** 123456

Good luck with your SIH presentation! 🚀
=======
# solar-microgrid-dashboard
IoT-based solar microgrid monitoring system for SIH
>>>>>>> c763254b9bd00e25e929de3747c22e6a8d47dcd1
