# 🏠 Alerta Urbana - Urban Security System

A comprehensive community security monitoring application that enables real-time surveillance, incident reporting, and emergency response coordination for residential areas.

## 🚀 Live Demo

**Try the interactive demo:** [View Demo](https://alvaro-oliveros.github.io/alerta-urbana/)

**Demo Credentials:**
- Email: `demo@alertaurbana.com`
- Password: `demo123`

## ✨ Features

### 🔐 **User Authentication & Profiles**
- Secure login and registration system
- User verification and profile management
- Session persistence with localStorage

### 📹 **Real-time Camera Monitoring**
- Live security camera feeds
- Expandable full-screen camera views
- Multiple camera locations (entrance, residential, parking)

### 🚨 **Enhanced Alert System**
- Severity-based alerts (Critical, High, Medium, Low)
- Real-time notifications
- Alert acknowledgment and status tracking
- Filter alerts by type and status

### 🏥 **Emergency Response**
- One-tap emergency calls (Police, Fire, Medical)
- Panic button with location sharing
- Emergency contact integration

### 📝 **Incident Reporting**
- Detailed incident reporting forms
- Location-based reporting
- Audio recording capability
- Report status tracking

### 🏆 **Community Engagement**
- User ranking system
- Points and rewards program
- Community participation tracking

### 📱 **Mobile-First Design**
- Responsive design optimized for mobile devices
- Touch-friendly interface
- iOS/Android compatible

## 🛠️ Technologies Used

- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Design:** Mobile-first responsive design
- **Storage:** Browser localStorage for session management
- **Security:** Input validation and secure authentication

## 📂 Project Structure

```
alerta-urbana/
├── index.html           # Main application file
├── index.md             # Redirect file for GitHub Pages
├── cameras/             # Security camera images
│   ├── 1.jpg           # Storage area camera
│   ├── 2.jpg           # Night vision driveway
│   └── 3.jpg           # Residential parking
├── README.md           # Project documentation
└── demo-setup.md       # Demo presentation guide
```

## 🚀 Getting Started

### Local Development
1. Clone the repository
```bash
git clone https://github.com/alvaro-oliveros/alerta-urbana.git
cd alerta-urbana
```

2. Serve locally
```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server

# Or simply open alerta_urbana.html in your browser
```

3. Open `http://localhost:8000` in your browser

### GitHub Pages Deployment
1. Go to repository Settings
2. Navigate to Pages section
3. Select "Deploy from a branch"
4. Choose "main" branch
5. Your app will be live at: `https://alvaro-oliveros.github.io/alerta-urbana/`

## 💡 Demo Instructions

Perfect for presentations and pitches:

1. **Share the live demo URL** or QR code with your audience
2. **Guide them through login** with the demo credentials
3. **Explore features together:**
   - Dashboard overview
   - Camera monitoring
   - Emergency features
   - Alert management
   - Community ranking

## 🔧 Configuration

The app includes demo data and simulated functionality. For production deployment:

- Replace demo authentication with real user management
- Integrate with actual security camera systems
- Connect to real emergency services APIs
- Implement backend database for persistent data storage

## 📊 Key Metrics

- **Response Time:** < 2 seconds for alert acknowledgment
- **Mobile Compatibility:** iOS 12+, Android 8+
- **Offline Support:** Core features available offline
- **Security:** Input validation and XSS protection

## 🎯 Use Cases

- **Residential Communities:** Gated communities, apartment complexes
- **Small Businesses:** Retail stores, offices
- **Educational Institutions:** Schools, universities
- **Public Spaces:** Parks, parking areas

## 🤝 Contributing

This is a demo project created for presentation purposes. For questions or suggestions, please contact [your-email@example.com].

## 📄 License

This project is created for demonstration and educational purposes.

---

**Built with ❤️ for urban security and community safety**