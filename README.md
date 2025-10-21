# 🪔 Diwali Diya Game - Technical Documentation

## Overview
An interactive Diwali celebration game built with pure HTML5, CSS3, and JavaScript. Players must light all 5 diyas within 10 seconds to win and enjoy a spectacular fireworks display.

## Technical Requirements ✅

### Core Technologies (No External Libraries)
- ✅ **HTML5** - Semantic markup with proper structure
- ✅ **CSS3** - Modern styling with animations and gradients
- ✅ **JavaScript (ES6+)** - Vanilla JavaScript for game logic
- ✅ **Canvas API** - Single canvas element for fireworks/confetti effects
- ✅ **Web Audio API** - Background music functionality

### Semantic HTML Structure
```
<main>
  <header>           - Game title and sound toggle
  <section.timer>    - Countdown timer section
  <section.diyas>    - Interactive diyas section
  <section.message>  - Win/lose message section
  <footer>           - Instructions
</main>
```

### Features Implemented

#### 1. **Gameplay Mechanics**
- ✅ 5 unlit diyas displayed centered on screen
- ✅ Click-to-light functionality with smooth animations
- ✅ 10-second countdown timer (auto-starts on page load)
- ✅ Win condition: All 5 diyas lit before timer ends
- ✅ Lose condition: Timer ends before all diyas are lit

#### 2. **Win State**
- ✅ Glowing message: "🎇 You spread the light faster than darkness! Happy Diwali 🎆"
- ✅ Fireworks/confetti animation using Canvas API
- ✅ Multi-location fireworks explosion (5 positions)
- ✅ Screen-wide celebration glow effect
- ✅ Animated text with shimmer effect

#### 3. **Lose State**
- ✅ Message: "⏳ Time's up! Try again and spread the light!"
- ✅ 'Try Again' button to restart game
- ✅ Complete game state reset

#### 4. **UI/UX Design**
- ✅ Dark purple/black animated gradient background
- ✅ Warm color tones (orange, gold, yellow)
- ✅ Modern Poppins font family
- ✅ Vertical and horizontal centering
- ✅ Glowing halos behind lit diyas
- ✅ Soft box-shadows and CSS transitions
- ✅ CSS flicker animation using @keyframes
- ✅ Festive gold-to-orange text gradients

#### 5. **Responsive Design**
- ✅ Desktop optimized (1200px+ screens)
- ✅ Tablet support (768px - 1199px)
- ✅ Mobile support (320px - 767px)
- ✅ Flexible layouts with proper scaling
- ✅ Touch-friendly tap targets

#### 6. **Optional Enhancements**
- ✅ Background music using Web Audio API
- ✅ Sound toggle button (🔇/🔊)
- ✅ Soft ambient tone that loops
- ✅ Visual feedback for sound state

#### 7. **Accessibility Features**
- ✅ ARIA labels for screen readers
- ✅ Keyboard navigation support (Tab, Enter, Space)
- ✅ Role attributes for semantic elements
- ✅ Live regions for dynamic content
- ✅ Proper focus management

#### 8. **Code Quality**
- ✅ Comprehensive inline comments
- ✅ Clear function documentation
- ✅ Organized code structure with sections
- ✅ Descriptive variable names
- ✅ Modular function design

#### 9. **Cross-Browser Compatibility**
- ✅ Chrome, Firefox, Safari, Edge support
- ✅ Vendor prefixes for CSS properties
- ✅ Fallback fonts for typography
- ✅ Cross-browser Audio API handling
- ✅ RequestAnimationFrame for smooth animations

## File Structure

```
diwali/
├── index.html          # Single self-contained file
└── README.md          # This documentation
```

## How to Run

1. Open `index.html` in any modern web browser
2. No server or build process required
3. Game starts automatically on page load

## How to Play

1. **Start**: Timer begins counting down from 10 seconds automatically
2. **Click**: Click on each diya to light it up
3. **Win**: Light all 5 diyas before timer reaches 0
4. **Sound**: Click the 🔇/🔊 button to toggle background music
5. **Retry**: If you lose, click "Try Again" to restart

## Game Components

### 1. Timer System
- Countdown from 10 seconds to 0
- Updates every 1000ms (1 second)
- Warning animation in last 3 seconds
- Automatic game end at 0

### 2. Diya Elements
- SVG-based graphics with gradients
- Warm color palette (gold, orange, brown)
- Unlit state (default)
- Lit state with flame and glow effects
- Hover animations for interactivity

### 3. Fireworks System
- Particle-based animation
- 50 particles per firework
- Physics simulation (gravity, velocity)
- Fade-out effect based on lifespan
- 5 staggered explosions on win

### 4. Sound System
- Web Audio API oscillator
- Sine wave at 200Hz
- Low volume (0.05) for ambiance
- Toggle on/off functionality
- Cross-browser compatible

## CSS Animations

### Keyframe Animations
1. **gradientShift** - Animated background gradient (15s loop)
2. **glowPulse** - Celebration glow pulsing effect (2s loop)
3. **timerBlink** - Timer warning flash (0.5s loop)
4. **flicker** - Realistic flame flicker (0.6s alternate)
5. **diyaGlow** - Lit diya glow animation (2s loop)
6. **haloGlow** - Halo expansion animation (2s loop)
7. **messageGlow** - Message entrance animation (1.2s)
8. **textShimmer** - Text brightness animation (2s loop)
9. **fadeInBounce** - Button bounce entrance (0.8s)

### Transitions
- Transform transitions with cubic-bezier easing
- Box-shadow smooth transitions
- Color transitions for hover states
- Opacity fades for messages

## Performance Optimizations

1. **RequestAnimationFrame** for smooth 60fps animations
2. **Particle cleanup** to remove dead particles
3. **Canvas clearing** between frames
4. **Event delegation** where appropriate
5. **CSS transforms** for hardware acceleration

## Browser Support

| Browser | Version | Status |
|---------|---------|--------|
| Chrome  | 90+     | ✅ Full |
| Firefox | 88+     | ✅ Full |
| Safari  | 14+     | ✅ Full |
| Edge    | 90+     | ✅ Full |
| Mobile Safari | 14+ | ✅ Full |
| Chrome Mobile | 90+ | ✅ Full |

## Color Palette

### Background
- `#0a0015` - Deep purple/black
- `#1a0033` - Dark purple
- `#2d1b4e` - Medium purple

### Diya Colors (Warm Tones)
- `#ffd700` - Gold
- `#daa520` - Goldenrod
- `#ff8c00` - Dark orange
- `#ff8c42` - Light orange
- `#cd853f` - Peru brown
- `#8b4513` - Saddle brown

### Flame Colors
- `#ff6b6b` - Coral red
- `#ffa502` - Orange
- `#ffd700` - Gold
- `#ffeb99` - Light yellow
- `#fff9e6` - Cream white

### Fireworks Colors
- `#ffd700` - Gold
- `#ff8c00` - Orange
- `#ff6347` - Tomato
- `#ff1493` - Deep pink
- `#00ff00` - Lime
- `#00ffff` - Cyan
- `#ffb347` - Light orange

## Code Statistics

- **Total Lines**: ~700
- **HTML**: ~80 lines
- **CSS**: ~400 lines
- **JavaScript**: ~220 lines
- **Comments**: ~150 lines
- **File Size**: ~35 KB

## Future Enhancement Ideas

- [ ] High score system with localStorage
- [ ] Difficulty levels (more diyas, less time)
- [ ] Different diya designs/patterns
- [ ] More firework patterns
- [ ] Achievement system
- [ ] Multiplayer mode
- [ ] Progressive Web App (PWA) support
- [ ] Share score on social media

## Credits

**Design & Development**: Complete implementation in single HTML file
**Font**: Google Fonts - Poppins
**Graphics**: SVG-based custom diya designs
**Animations**: Pure CSS3 and Canvas API

## License

Free to use for educational and personal projects.

---

**Happy Diwali! 🪔✨**

*May the festival of lights bring joy, prosperity, and happiness to all!*
