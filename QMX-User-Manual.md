# QMX Transceiver Interface - User Manual

## Table of Contents

1. [Introduction](#introduction)
2. [System Requirements](#system-requirements)
3. [Getting Started](#getting-started)
4. [Main Interface Overview](#main-interface-overview)
5. [Connection Setup](#connection-setup)
6. [Frequency Control](#frequency-control)
7. [Mode and Band Selection](#mode-and-band-selection)
8. [VFO Operations](#vfo-operations)
9. [Memory System](#memory-system)
10. [Audio Streaming](#audio-streaming)
11. [Spectrum Display and DSP](#spectrum-display-and-dsp)
12. [Voice Keyer](#voice-keyer)
13. [QSO Logger](#qso-logger)
14. [RIT Control](#rit-control)
15. [Controls and Meters](#controls-and-meters)
16. [Autotune Features](#autotune-features)
17. [Panel Management](#panel-management)
18. [Troubleshooting](#troubleshooting)
19. [Advanced Features](#advanced-features)

---

## Introduction

The QMX Transceiver Interface is a comprehensive web-based control application for QMX QRP transceivers. It provides advanced features including audio streaming, spectrum analysis, digital signal processing, voice keyer capabilities, and comprehensive logging functions.

### Key Features
- Real-time frequency and mode control
- Audio streaming with DSP filtering
- Spectrum analyzer display
- Voice message recording and playback
- Comprehensive QSO logging with ADIF support
- Memory channel management
- RIT (Receiver Incremental Tuning) control
- Autotune functionality
- Customizable panel layout

---

## System Requirements

### Browser Requirements
- Modern web browser with WebSerial API support:
  - Chrome 89+ (recommended)
  - Edge 89+
  - Opera 76+
- WebAudio API support for audio features

### Hardware Requirements
- QMX QRP transceiver
- USB cable for serial connection
- Computer with available USB port
- Microphone and speakers/headphones for audio features

### Permissions Required
- Serial port access
- Microphone access (for voice keyer and audio streaming)
- Speaker access (for audio output)

---

## Getting Started

### Initial Setup
1. Connect your QMX transceiver to your computer via USB
2. Open the QMX Interface in a compatible web browser
3. Allow browser permissions for serial port and microphone access when prompted
4. The interface will load with the default panel layout

### First Connection
1. Select the appropriate baud rate (usually 115200)
2. Click "Connect Serial" button
3. Select your QMX device from the browser's device list
4. Wait for "CONNECTED" status indication
5. The interface will automatically initialize the radio

---

## Main Interface Overview

The interface is organized into three main columns:

### Left Panel
- Serial connection controls
- Tuning step selection
- Mode selection buttons
- Band selection buttons
- Audio streaming controls
- CAT command log

### Center Panel
- Panel lock controls
- Main frequency display (LCD)
- Tuning knob
- Spectrum display with DSP controls
- VFO and transmit controls
- Status bar with time display

### Right Panel
- Voice keyer controls
- QSO logger
- Memory channel management
- Audio and RF controls
- S-meter and SWR meter
- RIT controls

---

## Connection Setup

### Serial Connection
1. **Baud Rate Selection**: Choose 115200 (standard for QMX)
2. **Connect Button**: Click to establish connection
3. **Status Indicators**: 
   - Green dot = Connected
   - Red dot = Disconnected
4. **Auto-initialization**: Radio settings are automatically synchronized

### Connection Health
- The interface monitors connection health
- Automatic reconnection attempts on disconnection
- Connection timeout detection and recovery

---

## Frequency Control

### Main Tuning Knob
- **Mouse Control**: Click and drag to tune
- **Wheel Control**: Mouse wheel for fine tuning
- **Keyboard Control**: Arrow keys when knob is focused
- **Hover Control**: Arrow keys when hovering over knob

### Direct Frequency Entry
- **LCD Click**: Click the frequency display to open entry modal
- **Format Options**: MHz, kHz, or Hz entry
- **Keypad**: Use on-screen keypad or keyboard
- **Validation**: Real-time frequency range checking

### Tuning Step Control
- **Step Sizes**: 1 Hz to 10 kHz
- **Variable Speed**: Automatic fast tuning detection
- **Visual Feedback**: Step size indicator

### Frequency Features
- **Band Auto-detection**: Automatic band selection based on frequency
- **Last Frequency Memory**: Remembers last frequency per band
- **Visual Effects**: Animated frequency changes

---

## Mode and Band Selection

### Mode Selection
Available modes:
- **USB**: Upper Sideband
- **LSB**: Lower Sideband  
- **CW**: Continuous Wave
- **DIGI**: Digital modes

### Band Selection
Supported amateur bands:
- **160m**: 1.8-2.0 MHz
- **80m**: 3.5-4.0 MHz
- **60m**: 5.33-5.405 MHz
- **40m**: 7.0-7.3 MHz
- **30m**: 10.1-10.15 MHz
- **20m**: 14.0-14.35 MHz
- **17m**: 18.068-18.168 MHz
- **15m**: 21.0-21.45 MHz
- **12m**: 24.89-24.99 MHz
- **10m**: 28.0-29.7 MHz
- **6m**: 50.0-54.0 MHz

### Band/Mode Interaction
- Mode selection affects DSP settings
- Band selection recalls last frequency for that band
- Visual indicators show active selections

---

## VFO Operations

### VFO Selection
- **VFO A**: Primary operating frequency
- **VFO B**: Secondary operating frequency
- **Visual Indication**: Active VFO highlighted in green

### VFO Functions
- **A↔B (Swap)**: Exchange frequencies between VFOs
- **A→B (Copy)**: Copy VFO A frequency to VFO B
- **Split Operation**: Use different VFOs for transmit/receive

### VFO Display
- Current VFO shown in LCD display
- Auto-detection from radio responses
- Manual selection available

---

## Memory System

### Memory Channels
- **10 Channels**: M1 through M10
- **Storage**: Frequency, mode, band, and optional label
- **Visual Indicators**: Occupied channels shown in green

### Memory Operations
- **Store Mode**: Click "Store" then channel to save current settings
- **Recall Mode**: Click "Recall" then channel to load settings
- **Edit Mode**: Click "Edit" then channel to modify stored data
- **Clear Mode**: Click "Clear" then channel to delete

### Advanced Memory Features
- **Quick Store**: Double-click any channel in recall mode
- **Memory Labels**: Custom text labels for identification
- **Import/Export**: Save/load memory sets as JSON files
- **Bulk Operations**: Clear all memories function

### Memory File Management
- **Export**: Save all memories to JSON file
- **Import**: Load memories from JSON file
- **Backup**: Regular memory backup recommended

---

## Audio Streaming

### Audio Setup
1. **Device Selection**: Choose input/output devices
2. **Refresh Devices**: Update available device list
3. **Gain Control**: Adjust audio amplification (1.0x to 5.0x)
4. **Level Monitoring**: Real-time input level display

### Audio Streaming Process
1. Select appropriate audio devices
2. Click "Start" to begin streaming
3. Monitor audio levels
4. Use "Stop" to end streaming

### Audio Features
- **Low Latency**: Optimized for real-time audio
- **Gain Boost**: Adjustable amplification
- **Level Meters**: Visual feedback of audio levels
- **Device Auto-selection**: Automatic device detection

### Audio Quality Settings
- **Sample Rate**: 48 kHz standard
- **Processing**: No noise reduction (for RF fidelity)
- **Latency**: Minimized for real-time operation

---

## Spectrum Display and DSP

### Spectrum Analyzer
- **Real-time Display**: Live audio spectrum visualization
- **Click-to-Tune**: Click peaks to auto-tune
- **Bandwidth Control**: Adjustable display range
- **Signal Detection**: Automatic signal identification

### CW DSP Filtering
Available only in CW mode:
- **Bandwidth Options**: 50 Hz to 300 Hz (native)
- **Filter Types**: Multiple filter stages for steep rolloff
- **Gain Compensation**: Automatic level adjustment
- **Real-time Control**: Instant filter parameter changes

### DSP Controls
- **Enable/Disable**: Toggle CW DSP processing
- **Bandwidth Selection**: Choose filter width
- **Target Pitch**: Set CW tone frequency (600-800 Hz)
- **Threshold Control**: Signal detection sensitivity

### Noise Floor Management
- **Auto-calibration**: Background noise measurement
- **Threshold Methods**: Statistical, percentile, or adaptive
- **Visual Indicators**: Optional noise floor display

---

## Voice Keyer

### Voice Message System
- **8 Message Slots**: Independent voice recordings
- **Current Slot Display**: Shows selected message
- **Slot Status**: Visual indication of recorded messages

### Recording Process
1. Select desired message slot (MSG 1-8)
2. Click "RECORD" to start recording
3. Speak your message
4. Click "STOP" when finished
5. Message automatically saved to selected slot

### Playback Operations
- **Manual Playback**: Click "PLAY" to transmit message
- **Auto TX/RX**: Automatic transmit control during playback
- **Stop Function**: Interrupt recording or playback
- **Clear Function**: Delete recorded message

### Voice Keyer Features
- **High Quality**: 64 kbps opus encoding
- **Device Selection**: Uses selected input device
- **Auto-transmit**: Optional automatic TX/RX switching
- **Message Status**: Real-time indication of occupied slots

---

## QSO Logger

### Contact Information
Required and optional fields:
- **Callsign**: Required field
- **RST Sent/Received**: Signal reports (default 599)
- **Name**: Contact's name
- **QTH**: Location information
- **Comments**: Additional notes

### Log Management
- **Real-time Info**: Current frequency, mode, band, and time
- **Auto-population**: Frequency and mode filled automatically
- **Search Function**: Filter logs by callsign
- **Contact Counter**: Total QSO count display

### ADIF Support
- **Export**: Generate ADIF files for other logging software
- **Import**: Load existing ADIF log files
- **Compatibility**: Standard ADIF format compliance
- **Duplicate Detection**: Prevents duplicate entries during import

### Log Features
- **Time Synchronization**: UTC time from internet time servers
- **Automatic Fields**: Frequency, mode, band auto-filled
- **Quick Entry**: Enter key logs current QSO
- **Data Validation**: Ensures required fields completed

---

## RIT Control

### RIT Functions
- **Enable/Disable**: Toggle RIT operation
- **Offset Control**: ±9999 Hz adjustment range
- **Clear Function**: Reset offset to zero
- **Fine Tuning**: Precise frequency adjustment

### RIT Operation
1. Click "RIT ON/OFF" to enable RIT
2. Use adjustment buttons for coarse changes (+/-1, +/-10, +/-100 Hz)
3. Use RIT knob for fine adjustments
4. Click "CLEAR" to reset offset

### RIT Display
- **Status Indicator**: Shows RIT on/off state
- **Offset Value**: Current RIT offset in Hz
- **Visual Feedback**: Active RIT indicated by green highlighting
- **Real-time Updates**: Immediate response to radio changes

---

## Controls and Meters

### Audio Gain (AF Gain)
- **Range**: 0-100% (logarithmic scaling)
- **Control**: Rotary knob interface
- **Display**: Percentage and dB indication
- **CAT Command**: AG command to radio

### CW Speed/Keyer Control
- **Modes**: STRAIGHT key or BUG (electronic keyer)
- **Speed Range**: 0-50 WPM
- **Mode Toggle**: Switch between straight key and keyer
- **Visual Indication**: Mode clearly displayed

### Power Control
- **Range**: 0-5.0 watts
- **Resolution**: 0.1 watt increments
- **Power Meter**: Real-time power output display
- **Safety**: QRP power levels only

### Meters
- **S-Meter**: Signal strength indication (S1-S9+)
- **SWR Meter**: Standing wave ratio during transmit
- **Power Meter**: Transmit power output
- **Audio Level**: Input audio monitoring

---

## Autotune Features

### Autotune Modes
- **Automatic**: Triggers after tuning stops
- **Manual**: On-demand scanning via button
- **Mode-Specific**: Different algorithms for CW and SSB

### Autotune Operation
1. Enable autotune feature
2. Tune near desired signal
3. Stop tuning and wait for automatic scan
4. Radio automatically adjusts to center signal

### Manual Scan
- **Instant Scan**: Click "AUTOTUNE CW/SSB NOW" button
- **Audio Required**: Must have audio streaming active
- **Visual Feedback**: Button flash indicates activation
- **Mode Sensitive**: Different algorithms for different modes

### Autotune Settings
- **Debounce Time**: Delay before automatic scan
- **Sensitivity**: Signal detection threshold
- **Frequency Range**: Scan bandwidth limits

---

## Panel Management

### Panel Layout
- **Draggable Panels**: Customize interface layout
- **Three Columns**: Left, center, and right panel areas
- **Persistent Layout**: Configuration saved automatically

### Panel Lock System
- **Lock Toggle**: Prevent accidental panel movement
- **Visual Indicators**: Lock status clearly shown
- **Quick Access**: Single button lock/unlock

### Layout Customization
1. Ensure panels are unlocked
2. Drag panel headers to desired locations
3. Drop panels in any column
4. Layout automatically saved
5. Lock panels when satisfied

---

## Troubleshooting

### Connection Issues
**Problem**: Cannot connect to radio
- Verify USB cable connection
- Check radio is powered on
- Try different baud rate
- Restart browser and try again

**Problem**: Frequent disconnections
- Check USB cable quality
- Verify driver installation
- Check for interference sources

### Audio Problems
**Problem**: No audio streaming
- Verify microphone permissions granted
- Check audio device selection
- Try refreshing audio devices
- Ensure devices are not in use by other applications

**Problem**: Poor audio quality
- Adjust audio gain settings
- Check microphone levels
- Verify sample rate compatibility

### Interface Issues
**Problem**: Frequency not updating
- Check CAT communication in log
- Verify radio responds to commands
- Try reconnecting serial connection

**Problem**: Erratic controls
- Check for multiple browser tabs
- Refresh page and reconnect
- Clear browser cache if needed

### Performance Issues
**Problem**: Slow response
- Close unnecessary browser tabs
- Check computer performance
- Disable browser extensions temporarily

---

## Advanced Features

### Time Synchronization
- **Internet Time**: Automatic UTC synchronization
- **Multiple Sources**: Fallback time servers
- **Radio Clock**: Sends time to QMX display
- **Logging Accuracy**: Precise QSO timestamps

### Effects and Animations
- **Visual Feedback**: Animated frequency changes
- **Sound Effects**: Optional audio feedback
- **Particle Effects**: Visual enhancement options
- **Customization**: Enable/disable individual effects

### Data Management
- **Local Storage**: Settings saved in browser
- **Export Functions**: Backup configurations
- **Import Capabilities**: Restore from files
- **Data Persistence**: Maintains settings between sessions

### CAT Command System
- **Command Queue**: Manages radio communication
- **Error Handling**: Automatic retry and recovery
- **Logging**: Complete command/response history
- **Debugging**: Detailed communication monitoring

### Keyboard Shortcuts
- **Tuning**: Arrow keys when hovering over knob
- **Enter**: Confirm frequency entry
- **Escape**: Cancel modal dialogs
- **Focus Control**: Tab navigation support

---

## Safety and Best Practices

### RF Safety
- Monitor power output levels
- Ensure proper antenna connections
- Check SWR before transmitting
- Follow local power restrictions

### Software Safety
- Regular backups of memory channels and logs
- Test features in receive mode first
- Monitor CAT command log for errors
- Keep browser updated for security

### Operating Practices
- Verify frequency before transmitting
- Check band plan compliance
- Monitor for other stations
- Use appropriate power levels

---

## Support and Resources

### Getting Help
- Check browser console for error messages
- Review CAT command log for communication issues
- Verify hardware connections
- Update browser to latest version

### Community Resources
- Amateur radio forums
- QMX user groups
- Software documentation
- Video tutorials

### AI Assistance
For customization and enhancements:
- Use Claude Sonnet 4, Gemini 2.5, or ChatGPT-5
- Ask for specific code snippets only
- Work incrementally on features
- Request placement instructions for code

---

*QMX Transceiver Interface - Professional QRP Communications Software*

*User Manual Version 1.0*

*© 2025 - Amateur Radio Software Project*