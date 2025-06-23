# Alerta Urbana - Demo Setup Guide

## Quick Deployment Steps

### Option 1: GitHub Pages (Recommended)
1. Create GitHub repository: `alerta-urbana-demo`
2. Upload `alerta_urbana.html` and `cameras/` folder
3. Go to Settings → Pages → Deploy from main branch
4. Your live URL: `https://yourusername.github.io/alerta-urbana-demo`

### Option 2: Netlify
1. Go to netlify.com
2. Drag & drop your project folder
3. Get instant URL

### Option 3: Local Network Demo
```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server

# Access via: http://your-laptop-ip:8000
```

## Demo Credentials
- **Email:** demo@alertaurbana.com
- **Password:** demo123

## QR Code Generation
1. Use qr-code-generator.com
2. Input your live URL
3. Download high-resolution QR code
4. Add to presentation slide

## Presentation Flow

### Slide 1: Problem Statement
- "Urban security challenges in residential areas"
- "Lack of real-time community monitoring"

### Slide 2: Solution Overview
- "Alerta Urbana - Community Security Platform"
- Show QR code: "Scan to try the demo"

### Slide 3: Live Demo
- "Everyone follow along on your phones"
- Walk through key features together

### Slide 4: Key Features Highlight
- User authentication & profiles
- Real-time camera monitoring
- Enhanced alert system with severity levels
- Community engagement (ranking/rewards)

### Slide 5: Technical Implementation
- Responsive mobile-first design
- Real-time notifications
- Secure user management

## Demo Script

1. **"Please scan the QR code and open the app"**
2. **"Login with: demo@alertaurbana.com / demo123"**
3. **"You're now in the dashboard - this is what residents see"**
4. **"Tap the camera icon - see live security feeds"**
5. **"Tap emergency - immediate access to help"**
6. **"Check alerts - real-time security notifications"**
7. **"View your profile - community engagement"**

## Backup Plans
- Have app pre-loaded on multiple devices
- Screenshot slides if network fails
- Local hotspot for internet backup