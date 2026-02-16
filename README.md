# Arduino LED Pattern Controller

A comprehensive Arduino project that controls multiple LEDs (0-13) to create various dynamic lighting patterns and sequences.

## 🎯 Project Overview

This Arduino sketch controls up to 14 LEDs connected to digital pins 0-13, creating a series of mesmerizing light patterns including:
- Color transitions building to white center
- Sequential blinking patterns
- Complex choreographed light shows
- Individual LED control sequences

## 📷 Project Documentation

### Setup Photo
![Arduino Setup](A_Arduino%20Image.jpg)

### Demo Video
[Watch the LED patterns in action](A_Final%20Video.mp4)

## 🔧 Hardware Requirements

- Arduino board (Uno, Nano, or similar)
- 14 LEDs
- 14 current-limiting resistors (220Ω recommended)
- Breadboard or PCB for connections
- Jumper wires
- Power supply (if needed for high-power LEDs)

## 🔌 Wiring Diagram

Connect LEDs to digital pins 0-13:
- LED 0 → Pin 0 → Resistor → Ground
- LED 1 → Pin 1 → Resistor → Ground
- LED 2 → Pin 2 → Resistor → Ground
- ...
- LED 13 → Pin 13 → Resistor → Ground

⚠️ **Note**: Pin 0 and 1 are used for serial communication. If you need serial debugging, consider using pins 2-13 only.

## 🎨 Pattern Descriptions

### Main Sequence
The main loop runs a carefully choreographed sequence:

1. **Color Transition Pattern** (`blink_1_to_10_colors`)
   - Builds lighting from edges (pins 1 & 10) toward center
   - Creates white center effect
   - 2-second build-up sequence

2. **Individual Patterns** (`blink_1` through `blink_16`)
   - Each function creates unique blinking sequences
   - Various timing and combinations
   - Some patterns commented out for customization

### Pattern Characteristics
- **Timing**: Carefully calibrated delays for smooth transitions
- **Symmetry**: Many patterns use symmetrical lighting (pins 1-10)
- **Modularity**: Each pattern is a separate function for easy modification

## 💻 Code Structure

```cpp
// Pin Definitions
int led0 = 0; // through led13 = 13;

// Setup - Initialize all pins as OUTPUT
void setup() { ... }

// Main Loop - Orchestrates pattern sequence
void loop() { ... }

// Pattern Functions
void blink_1_to_10_colors() { ... }
void blink_1() { ... }
// ... through blink_16()
```

## 🚀 Getting Started

1. **Hardware Setup**
   - Connect LEDs and resistors to pins 0-13 as described
   - Double-check all connections

2. **Software Setup**
   - Open `led_design.ino` in Arduino IDE
   - Select your board and port
   - Upload the sketch

3. **Customization**
   - Modify timing by changing `delay()` values
   - Enable/disable patterns by commenting/uncommenting function calls
   - Add new patterns by creating additional `blink_X()` functions

## 🎛️ Customization Options

### Timing Adjustments
- Modify `delay()` values to speed up or slow down patterns
- Standard delays: 50ms (quick), 200ms (medium), 1000ms+ (slow)

### Pattern Selection
- Comment out unwanted patterns in `loop()`
- Add new patterns by duplicating and modifying existing functions
- Create custom sequences by combining different LED combinations

### Hardware Modifications
- Use RGB LEDs for color effects
- Add more LEDs by expanding pin definitions
- Implement PWM for brightness control

## 🔧 Troubleshooting

**LEDs not lighting up:**
- Check wiring connections
- Verify resistor values (too high = dim, too low = risk of damage)
- Test individual LEDs with a multimeter

**Erratic patterns:**
- Ensure stable power supply
- Check for loose connections
- Verify pin assignments match physical connections

**Upload issues:**
- If using pins 0-1, disconnect LEDs during upload
- Select correct board and port in Arduino IDE

## 📝 Technical Notes

- **Total patterns**: 16+ individual functions
- **Code size**: ~2342 lines
- **Memory usage**: Optimized for Arduino Uno specifications
- **Timing precision**: Millisecond-level control

## 🎪 Demo Features

The video demonstration shows:
- Smooth color transitions
- Synchronized blinking sequences
- Complex multi-LED choreography
- Professional timing and flow

## 📜 License

This project is open source. Feel free to modify and share!

## 🤝 Contributing

Want to add new patterns or improve existing ones?
- Fork the project
- Create new pattern functions
- Test thoroughly with hardware
- Submit pull request with video demonstration

---

**Created with ❤️ for the Arduino community**