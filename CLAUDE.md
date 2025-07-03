# Alerta Urbana - Development Context

## Project Overview
Spanish urban security app called "Alerta Urbana" - a community security monitoring application with real-time surveillance, incident reporting, and emergency response coordination for residential areas.

**Live Demo:** https://alvaro-oliveros.github.io/alerta-urbana/
**Demo Credentials:** Email: `demo` | Password: `demo`

## Recent Development Session

### Main Features Implemented
1. **Alert Filtering System** - Complete filtering by severity, status, and time with search functionality
2. **Mobile Responsive Design** - Full screen on mobile, phone mockup on desktop
3. **iOS/Safari Compatibility** - Comprehensive keyboard handling and layout fixes
4. **Report Submission** - Enhanced with success notifications and form clearing
5. **Voice Recording Simulation** - Visual feedback with timer and state management

### Key Technical Achievements

#### Alert Filtering & Search (Centro de Alertas)
- **Search Bar**: Real-time search through alert content with clear button
- **Severity Filters**: Critical, High, Medium, Low with visual indicators
- **Status Filters**: Pending, Acknowledged, All with proper state tracking
- **Time Filters**: Última hora (last hour), Hoy (today), Esta semana (this week), Todo (all)
- **Combined Filtering**: All filters work together with live result counting
- **Spanish Time Parsing**: Fixed "última hora" filter to properly parse Spanish time expressions like "hace 2 min" vs "hace 1h 15min"

#### Mobile Responsiveness & Browser Compatibility
- **Desktop**: 450px wide phone mockup with 2x2 action card grid
- **Mobile**: Full viewport (100vw x 100vh) with fixed status bar and navigation
- **iOS Keyboard Handling**: Visual Viewport API integration with dynamic layout switching
- **Safari-Specific Fixes**: Bottom content visibility with address bar compensation
- **Cross-Platform**: Works on Chrome, Safari (both mobile and desktop)

#### Report Submission & Voice Recording
- **Success Notifications**: "✅ Reporte enviado exitosamente" popup after submission
- **Form Clearing**: All fields reset including camera selector, location, description, photos, and audio
- **Voice Recording Simulation**: 
  - Button changes to red ⏹️ with scale and glow effects
  - Timer counts up in MM:SS format with red styling
  - Completion popup shows recording duration
  - Proper state reset after form submission

### Critical Bug Fixes

#### 1. Alert Acknowledge Functionality
**Issue**: Specific alerts ("Movimiento Detectado", "Vehículo No Autorizado") wouldn't mark as acknowledged
**Root Cause**: DOM element duplication between dashboard and alert center
**Solution**: Targeted only `#alerts` selectors with dashboard synchronization

#### 2. Time Filter Logic  
**Issue**: "última hora" filter showing empty results or incorrect alerts
**Root Cause**: Pattern matching for "h" was catching "hace" (Spanish for "ago")
**Solution**: More specific regex pattern `/\d+h/` to identify actual hour indicators

#### 3. Mobile Layout Issues
**Issue**: Status bar and navigation not staying fixed on mobile during keyboard input
**Root Cause**: Viewport changes from virtual keyboard conflicting with fixed positioning
**Solution**: Dynamic layout switching between fixed and relative positioning modes

#### 4. Desktop Grid Layout
**Issue**: Quick action cards showing as 4x1 column instead of 2x2 grid on desktop
**Root Cause**: Phone container too narrow (375px) for proper grid layout
**Solution**: Increased desktop container width to 450px with high-specificity CSS

#### 5. Function Definition Order
**Issue**: "toggleRecording is not defined" error when clicking microphone button
**Root Cause**: Function defined after HTML onclick handlers tried to use it
**Solution**: Moved functions to top of script with immediate global assignment

### File Structure
```
/Users/alvaro/Desktop/alerta_urbana/
├── index.html              # Main application (single file)
├── cameras/                 # Security camera images (1.jpg, 2.jpg, 3.jpg)
├── README.md               # Project documentation
├── demo-setup.md           # Presentation setup guide
├── index.md                # GitHub Pages redirect
├── .claude/settings.local.json  # Git permissions
└── CLAUDE.md               # This context file
```

### Code Architecture
- **Single Page Application**: Everything in index.html (HTML + CSS + JavaScript)
- **Screen Navigation**: JavaScript-based screen switching with CSS transitions
- **Mobile-First Design**: Responsive CSS with desktop overrides
- **Global Functions**: Key functions assigned to window object for onclick handlers

### Testing Checklist
- ✅ Alert filtering works across all combinations (severity + status + time + search)
- ✅ Mobile responsive on iPhone 15 (Safari and Chrome)
- ✅ Desktop 2x2 grid layout in phone mockup
- ✅ Report submission with success notification and form clearing
- ✅ Voice recording with visual feedback and timer reset
- ✅ Acknowledge buttons work for all alerts with visual feedback
- ✅ Keyboard handling on iOS without layout breaks

### Development Notes
- **CSS Specificity**: Use `!important` and ID selectors for critical layout rules
- **Mobile Keyboard**: Visual Viewport API preferred over resize events for iOS
- **Function Timing**: Define functions early in script before HTML references them
- **Spanish Localization**: Consider language-specific parsing for time expressions
- **Browser Detection**: Safari requires different safe-area-inset handling

### Next Steps for Production
1. Replace demo authentication with real user management
2. Integrate with actual security camera systems  
3. Connect to real emergency services APIs
4. Implement backend database for persistent data storage
5. Add push notification service
6. Optimize for larger screen sizes beyond phone mockup

### Presentation Ready
The app is fully optimized for live demonstrations with:
- Seamless mobile experience for audience participation
- No scrolling or layout issues across devices
- Professional visual feedback for all interactions
- Quick demo flow: Login (demo/demo) → Dashboard → Features → Reports → Alerts