# QMX Interface with new GUI and Spectrum Display


![GitHub Pages](https://img.shields.io/github/deployments/Sparks72/QMX-new-GUI/github-pages?label=GitHub%20Pages)
![GitHub last commit](https://img.shields.io/github/last-commit/Sparks72/QMX-new-GUI)
![GitHub repo size](https://img.shields.io/github/repo-size/Sparks72/QMX-new-GUI)
![License](https://img.shields.io/badge/license-Amateur%20Radio-blue)
![Browser Support](https://img.shields.io/badge/browser-Chrome%20%7C%20Edge%20%7C%20Opera-green)



A comprehensive web-based control interface for the QMX QRP transceiver, providing advanced features for amateur radio operators including CAT control, audio streaming, spectrum analysis, and automated tuning capabilities.

## 🌐 Live Demo

**[Try the Live Demo Here](https://sparks72.github.io/QMX-new-GUI/)**
The live demo runs entirely in your browser - no installation required! You can explore the full interface even without a connected radio. For full functionality, connect your QMX transceiver via USB.

### Quick Demo Instructions
1. Click the live demo link above
2. Grant microphone permission for audio features (optional)
3. Explore the interface without hardware
4. Connect your QMX for full CAT control functionality

## Screenshots

**Main Interface Overview**
![Main Interface](screenshot1.png)
*The complete QMX+ interface showing the customizable panel layout with frequency display, tuning controls, and AutoTune Spectrum*

**Advanced Features in Action**
![Advanced Features](screenshot2.png)
*Spectrum analyzer, memory channels, QSO logger, and audio streaming controls in operation*



## GETTING STARTED

**Connection**
- Select baud rate (default: 115200)
- Click "Connect" to establish serial connection
- Green status dot = connected
- Audio streaming and radio control are independent

---

## FREQUENCY CONTROL

**Main Tuning Knob**
- **Click & drag**: Rotate to tune
- **Mouse wheel**: Fine tuning
- **Arrow keys** (when focused): Adjust frequency
- **Hover + arrow keys**: Quick adjustment without clicking
- Variable speed tuning: Tune fast for automatic 10x step increase

**Direct Entry**
- Click LCD display to open frequency input modal
- Choose format: MHz / kHz / Hz
- Use keypad or type directly
- Press Enter or click "Set"

**Tuning Step**
- Select step size: 1 Hz to 10 kHz
- Saved automatically between sessions

---

## MODE & BAND SELECTION

**Modes**: USB, LSB, CW, DIGI
- Click mode button to change
- Mode affects spectrum bandwidth and DSP filtering

**Bands**: 160m to 6m (11 bands including 60m)
- Click band button to change
- Last-used frequency per band remembered
- Auto band selection based on frequency

---

## VFO CONTROL

**VFO A / VFO B**
- Click to select active VFO
- Each VFO has independent frequency

**VFO Operations**
- **A↔B**: Swap VFO A and B frequencies
- **A→B**: Copy VFO A to VFO B (or B→A depending on active VFO)

---

## AUDIO STREAMING

**Setup**
1. Click "Refresh" to enumerate audio devices
2. Select Input device (from QMX)
3. Select Output device (PC speakers)
4. Click "Start"

**Audio Gain Control**
- Slider: 0.1x to 5.0x (default: 2.0x)
- Displayed in multiplier and dB
- Adjusts real-time during streaming

**CW DSP Filter** (CW mode only)
- Bandwidth: 50 Hz to 300 Hz
- Target pitch: 600/700/800 Hz
- Check "ON" to enable
- Multiple noise floor detection methods
- "Calibrate Noisefloor" for optimal settings

---

## SPECTRUM DISPLAY

**Features**
- Real-time FFT spectrum analyzer
- Signal/noise discrimination
- Click spectrum to auto-tune to signal
- Bandwidth adjusts with mode and DSP settings

**Signal Detection**
- Threshold slider: Sensitivity adjustment
- Noise floor methods: Auto / Avg / Adapt
- Show noise floor line (yellow)

---

## AUTOTUNE

**Manual Scan**
- Click "AUTOTUNE CW/SSB NOW" to scan once
- Works in CW and SSB modes
- Starts audio stream if not already running

**Auto Mode**
- Toggle "AUTOTUNE ON/OFF"
- Scans automatically after tuning stops (750ms delay)
- Centers signal on target pitch (CW) or 1500 Hz (SSB)

---

## MEMORY CHANNELS (M1-M10)

**Modes**: Recall / Store / Edit / Clear
- Click mode button, then click memory slot

**Quick Operations**
- **Single click** (Recall mode): Load frequency/mode/band
- **Double click** (Recall mode): Quick-store current settings
- **Right-click**: Open edit modal

**Edit Modal**
- Set frequency, mode, band manually
- Add optional label
- Press Enter in frequency field to save quickly

**Management**
- Export: Save to JSON file
- Import: Load from JSON file
- Clear All: Delete all memories

---

## CW KEYER MEMORY (8 Slots)

**Message Storage**
1. Type message (max 80 characters, auto-uppercase)
2. Select slot (CW1-CW8)
3. Click "STORE"

**Sending**
- Click "SEND" or select slot to transmit
- **F1-F8**: Quick send from keyboard
- Status shows buffer state during transmission

**Editing**
1. Click "EDIT" button (activates edit mode)
2. Select slot to edit
3. Modal opens with message text and label fields
4. Save changes

**Management**
- Export/Import: Save/load messages to JSON
- Clear All: Delete all stored messages

---

## CW SPEED CONTROL

**Two Synchronized Knobs**
- Controls Panel: Main RF Gain knob
- CW Keyer Panel: Clone knob
- Both knobs mirror each other

**Keyer Mode Toggle**
- **STRAIGHT**: 0 WPM (straight key mode)
- **BUG**: 1-50 WPM (electronic keyer)

**Adjustment**
- Click & drag, mouse wheel, arrow keys
- Hover + arrow keys for quick adjustment
- Knobs dim/disable in STRAIGHT mode

---

## CW SPEED CONTROL

**Two Synchronized Knobs**
- Controls Panel: Main RF Gain knob
- CW Keyer Panel: Dedicated CW Speed knob (clone)
- Both knobs mirror each other in real-time
- Adjust either knob, both update simultaneously

**Keyer Mode Toggle**
- **STRAIGHT**: 0 WPM (straight key mode)
- **BUG**: 1-50 WPM (electronic keyer)
- Toggle switch appears on both panels

**Adjustment**
- Click & drag to rotate
- Mouse wheel for fine adjustment
- Arrow keys when focused
- **Hover + arrow keys**: Quick adjustment without clicking (works on both knobs)
- Visual feedback: Green glow on hover, bright flash on keypress
- Knobs automatically dim and disable in STRAIGHT mode

**Speed Range**
- 0 WPM (Straight key)
- 1-50 WPM (Bug/Electronic keyer)
- Display shows current speed or "STRAIGHT"
- Color coded: Red (0 WPM), Green (1-50 WPM)

---

## VOICE KEYER (8 Slots)

**Recording**
1. Select message slot (MSG 1-8)
2. Click "RECORD"
3. Speak message
4. Click "STOP"
- Volume auto-mutes during recording
- Audio streaming auto-pauses if active

**Playback**
- Click "PLAY" to transmit message
- **Shift + F1-F8**: Quick playback from keyboard
- Auto TX/RX: Automatically keys transmitter

**Management**
- Stored in browser localStorage (persistent)
- Export/Import: Save/load metadata only
- Clear: Delete individual or all messages
- Volume auto-restores after playback

---

## RIT (RECEIVER INCREMENTAL TUNING)

**Controls**
- **RIT ON/OFF**: Enable/disable RIT
- **CLEAR**: Reset offset to 0 Hz
- Fine tune knob: ±1000 Hz range

**Adjustment Buttons**
- ±1 Hz, ±10 Hz, ±100 Hz
- Display shows offset with +/- color coding

**Features**
- Green glow when active
- Knob responds to mouse, wheel, keyboard
- Range: ±9999 Hz

---

## QSO LOGGER

**Logging**
1. Enter callsign (auto-uppercase)
2. Optional: Name, QTH, RST, comments
3. Click "Log QSO"
- Frequency, mode, band, UTC time auto-filled

**Features**
- Search by callsign
- Export to ADIF format
- Import ADIF files
- Shows total QSO count

---

## CONTROLS PANEL

**AF Gain (Volume)**
- 0-100 dB
- Click & drag, wheel, arrow keys
- Hover + arrow keys for quick control
- Auto-mutes during voice recording

**Power Out**
- 0-5.0W (QRP)
- Displays in watts
- Color coded: green → yellow → red

---

## PANEL MANAGEMENT

**Lock/Unlock Panels**
- Click "🔓 Panels Unlocked" to lock
- When locked: 🔒 icon shows, no dragging
- When unlocked: Drag panels by title bar

**Layout**
- Drag panels between left/center/right columns
- Layout saved automatically
- Survives page reload

---

## ZOOM & FULLSCREEN

**Zoom Controls** (top right)
- **+/-**: Zoom in/out (50%-200%)
- **Reset**: Return to 100%
- **Fit**: Auto-fit to window
- **⛶**: Toggle fullscreen

**Keyboard Shortcuts**
- Ctrl + Plus: Zoom in
- Ctrl + Minus: Zoom out
- Ctrl + 0: Reset zoom
- F11: Toggle fullscreen

---

## KEYBOARD SHORTCUTS

**CW Keyer**
- **F1-F8**: Send CW message from slot 1-8

**Voice Keyer**
- **Shift + F1-F8**: Play voice message from slot 1-8

**Memory Channels**
- **Right-click** memory button: Edit

**Frequency Control**
- **Arrow keys** (when knob focused): Tune
- **Arrow keys** (when hovering): Quick tune
- **Enter** (in frequency input): Confirm

---

## TIPS & TROUBLESHOOTING

**Audio Issues**
- Click "Refresh" if devices not showing
- Browser needs microphone permission
- Use specific device, not "default"
- Disable echo cancellation in device settings

**Connection Problems**
- Try different baud rates
- Reconnect USB cable
- Check serial port permissions
- Green status dot confirms connection

**Performance**
- Disable unused features
- Lower spectrum FFT size if laggy
- Close other browser tabs

**Data Persistence**
- Memory channels: Saved in browser
- Voice messages: Saved in browser (limited by storage quota)
- CW messages: Saved in browser
- Panel layout: Saved in browser
- Step size: Saved in browser
- Last frequencies per band: Saved

**Best Practices**
- Export memories/messages regularly
- Test voice messages before operating
- Calibrate noise floor in quiet conditions
- Use autotune for weak signals
- Lock panels during operation

---

## Development

### Local Development
1. Clone this repository
2. Open `index.html` in a supported browser
3. No build process required - pure HTML/CSS/JavaScript

### Contributing
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

### File Structure
```
QMX+ Interface/
├── index.html           # Main application
├── screenshot1.png      # Interface overview
├── screenshot2.png      # Advanced features
├── README.md           # This documentation
└── .github/
    └── workflows/
        └── pages.yml    # GitHub Pages deployment
```

## Technical Details

### CAT Commands
The interface uses standard Kenwood CAT commands:
- `FA`/`FB`: VFO A/B frequency
- `MD`: Mode control
- `IF`: Information request
- `AG`: AF Gain
- `KS`: Keyer speed
- `RT`/`RU`/`RD`: RIT control

### Data Storage
- Panel layouts saved to localStorage
- Memory channels saved to localStorage  
- QSO log saved to localStorage
- Last frequencies per band saved

### Audio Processing
- 48 kHz sample rate
- Real-time spectrum analysis via Web Audio API
- Adjustable gain control
- Peak detection for click-to-tune

## Browser Compatibility

| Browser | Version | WebSerial | Audio API | Status |
|---------|---------|-----------|-----------|--------|
| Chrome | 89+ | ✅ | ✅ | Fully Supported |
| Edge | 89+ | ✅ | ✅ | Fully Supported |
| Opera | 75+ | ✅ | ✅ | Fully Supported |
| Firefox | Any | ❌ | ✅ | Audio Only |
| Safari | Any | ❌ | ✅ | Audio Only |

## Support

For issues, questions, or feature requests:
- Open an issue on this repository
- Check browser console for error messages
- Verify WebSerial API support
- Ensure proper hardware connections

## License

Apache 2.0
