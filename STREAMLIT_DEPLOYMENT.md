# 🌞 Solar Microgrid Dashboard - Streamlit Deployment

## 📋 Overview

This is a complete single-file Streamlit application for your SIH demo that includes:

- ✅ **Real-time data simulation** - No hardware required
- ✅ **Beautiful dashboard** with animations and modern UI
- ✅ **Authentication system** - Phone number + OTP login
- ✅ **Alert management** - Smart alerts with 1-minute intervals
- ✅ **Interactive charts** - Real-time energy, battery, and efficiency monitoring
- ✅ **Responsive design** - Works on desktop, tablet, and mobile
- ✅ **Professional UI** - Glassmorphism effects and smooth animations

## 🚀 Quick Start

### Option 1: Using the deployment script (Recommended)
```bash
./deploy-streamlit.sh
```

### Option 2: Manual installation
```bash
# Install dependencies
pip3 install -r requirements-streamlit.txt

# Run the application
streamlit run deploy-streamlit.py
```

### Option 3: One-line command
```bash
pip3 install streamlit plotly pandas numpy && streamlit run deploy-streamlit.py
```

## 🌐 Access the Dashboard

Once started, open your browser and go to:
- **Local:** http://localhost:8501
- **Network:** http://your-ip:8501

## 🔑 Demo Credentials

- **Phone Number:** Any number (e.g., 9845280208)
- **OTP:** 123456

## 📱 Features

### 🔐 Authentication
- Phone number-based login
- OTP verification (demo: 123456)
- Session management
- Secure operator profiles

### 📊 Real-time Dashboard
- **Energy Metrics:** Generation, Storage, Load, Efficiency
- **Weather Data:** Temperature, Solar Irradiance
- **System Status:** Health indicators and uptime
- **Alert System:** Smart notifications with severity levels

### 📈 Interactive Charts
- **Energy Chart:** Generation vs Load over time
- **Battery Chart:** State of Charge with threshold lines
- **Efficiency Chart:** System performance monitoring
- **Real-time Updates:** Auto-refresh every 5 seconds

### 🚨 Alert System
- **Critical Alerts:** Battery < 30%, Temperature > 40°C
- **Warning Alerts:** Battery < 50%, Temperature > 35°C
- **Smart Timing:** Alerts sent once per minute (no spam)
- **Visual Indicators:** Color-coded severity levels

### 🎨 Beautiful UI
- **Modern Design:** Glassmorphism and gradient effects
- **Smooth Animations:** Fade-in, pulse, and hover effects
- **Responsive Layout:** Works on all screen sizes
- **Professional Theme:** Custom CSS styling

## 🛠️ Technical Details

### Dependencies
- **Streamlit:** Web application framework
- **Plotly:** Interactive charts and graphs
- **Pandas:** Data manipulation and analysis
- **NumPy:** Numerical computing
- **Python-dateutil:** Date and time utilities

### Data Simulation
- **1000 data points** of historical energy and weather data
- **5-second intervals** for real-time simulation
- **Daily patterns** with realistic variations
- **No external APIs** required - completely self-contained

### Alert Logic
- **Battery SOC:** Critical < 30%, Warning < 50%
- **Temperature:** Critical > 40°C, Warning > 35°C
- **Generation:** Warning < 1000W
- **Efficiency:** Warning < 75%
- **Smart timing:** 1-minute intervals to prevent spam

## 📱 Mobile Support

The dashboard is fully responsive and works great on:
- 📱 **Mobile phones** (iOS/Android)
- 📱 **Tablets** (iPad/Android tablets)
- 💻 **Desktop computers**
- 🖥️ **Large screens**

## 🎯 Perfect for SIH Demo

### What Judges Will See:
1. **Professional Login** - Phone number authentication
2. **Real-time Dashboard** - Live data updates every 5 seconds
3. **Beautiful Charts** - Interactive energy monitoring
4. **Smart Alerts** - Professional notification system
5. **Mobile Responsive** - Works on any device
6. **No Hardware Required** - Pure software simulation

### Demo Flow:
1. **Open** http://localhost:8501
2. **Login** with any phone number + OTP: 123456
3. **Observe** real-time dashboard with live data
4. **Interact** with charts and metrics
5. **Experience** professional alert system
6. **Show** mobile responsiveness

## 🔧 Customization

### Changing Alert Thresholds
Edit the `check_alerts()` function in `deploy-streamlit.py`:
```python
# Battery alerts
if energy_data['storage_soc_percent'] < 30:  # Change threshold here
    # Critical alert logic

# Temperature alerts  
if weather_data['temp_c'] > 40:  # Change threshold here
    # Critical alert logic
```

### Modifying Data Patterns
Edit the `generate_historical_data()` function:
```python
# Energy data with daily patterns
generation = 1800 + 600 * np.sin(2 * np.pi * hours / 24) + np.random.normal(0, 100, 1000)
# Modify the base values and patterns here
```

### Customizing UI Colors
Edit the CSS variables in the `st.markdown()` section:
```css
:root {
    --primary-color: #1f77b4;    /* Change primary color */
    --secondary-color: #ff7f0e;  /* Change secondary color */
    --success-color: #2ca02c;    /* Change success color */
    --warning-color: #d62728;    /* Change warning color */
}
```

## 🚀 Deployment Options

### Local Development
```bash
streamlit run deploy-streamlit.py
```

### Production Deployment
```bash
streamlit run deploy-streamlit.py --server.port 8501 --server.address 0.0.0.0
```

### Cloud Deployment
- **Streamlit Cloud:** Upload to GitHub and deploy
- **Heroku:** Add Procfile and deploy
- **Railway:** Connect GitHub repository
- **AWS/GCP/Azure:** Use container services

## 📞 Support

For issues or questions:
1. Check the console output for error messages
2. Ensure all dependencies are installed correctly
3. Verify Python 3.7+ is being used
4. Check if port 8501 is available

## 🎉 Success!

Your Solar Microgrid Dashboard is now ready for the SIH presentation! 

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
