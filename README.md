# AI-Virtual-Keyboard
# Virtual AI Keyboard

A gesture-based virtual keyboard that allows you to type using hand gestures captured via webcam. This innovative application uses computer vision to detect finger movements and translates them into keyboard inputs.


## ✨ Features

- **Touchless Typing**: Type without physical contact using hand gestures
- **Real-Time Hand Tracking**: Accurate detection of 21 hand landmarks using MediaPipe
- **Dynamic Text Display**: Auto-expanding text area with word wrapping
- **Visual Feedback**: Clear indicators for key activation and shift status
- **Full Keyboard Functionality**: Support for letters, punctuation, and special keys
- **Cross-Platform**: Works on Windows, macOS, and Linux
- **Customizable Layout**: Easily modify keyboard layout and appearance

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- Webcam
- pip (Python package manager)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/virtual-ai-keyboard.git
cd virtual-ai-keyboard
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

### Usage

1. Run the application:
```bash
python main.py
```

2. Position your hand in view of the webcam
3. Move your index finger over the desired key
4. Pinch your thumb and index finger together to "press" the key
5. Use the special keys:
   - **Shift**: Toggle uppercase characters
   - **Space**: Insert space
   - **Ent**: Enter key
   - **Bac**: Backspace
   - **Clear**: Clear all text

6. Press 'q' to quit the application

## ⌨️ Keyboard Layout

The virtual keyboard follows this layout:

```
Q   W   E   R   T   Y   U   I   O   F
A   S   D   F   G   H   J   K   L   ;
Shift  Z   X   C   V   B   N   M   ,   .
Space  Ent  Bac  Clear
```

## 🛠️ Customization

You can easily customize the keyboard by modifying the `KEYBOARD_LAYOUT` array in `main.py`:

```python
KEYBOARD_LAYOUT = [
    ["Q", "W", "E", "R", "T", "Y", "U", "I", "O", "P"],
    ["A", "S", "D", "F", "G", "H", "J", "K", "L", ";"],
    ["Shift", "Z", "X", "C", "V", "B", "N", "M", ",", "."],
    ["Space", "Ent", "Bac", "Clear"]
]
```

Adjust detection sensitivity by changing these parameters:
```python
self.detector = HandDetector(detectionCon=0.7, maxHands=1)  # Lower = more sensitive
length < 45  # Increase for easier activation
```

Change colors by modifying the `COLORS` dictionary:
```python
self.COLORS = {
    "primary": (255, 0, 0),    # Blue instead of pink
    "highlight": (0, 255, 255),# Cyan instead of green
    # ... other color values
}
```

## 📁 Project Structure

```
virtual-ai-keyboard/
│
├── main.py                 # Main application file
├── requirements.txt        # Project dependencies
├── README.md              # Project documentation
├── LICENSE                # MIT License
├── assets/                # Resources folder
│   ├── demo.gif           # Application demo
│   └── screenshot.png     # Application screenshot
└── examples/              # Usage examples
    └── basic_usage.py     # Basic implementation example
```

## 🎯 How It Works

1. **Hand Detection**: Uses CVZone's HandDetector module based on MediaPipe to detect hands and 21 landmarks
2. **Gesture Recognition**: Identifies pinch gestures between index finger and thumb for key presses
3. **Virtual Keyboard Rendering**: Draws a customizable keyboard layout on the video feed
4. **Input Simulation**: Uses pynput to simulate actual keyboard input
5. **Text Display**: Implements dynamic text area with word wrapping for long content

## 🔧 Technical Details

### Dependencies

- **OpenCV**: Computer vision library for image processing
- **NumPy**: Numerical computing library
- **CVZone**: Simplified computer vision utilities built on MediaPipe
- **pynput**: Cross-platform input control library

### Key Components

- **HandDetector**: Detects and tracks hand landmarks in real-time
- **Keyboard Controller**: Simulates physical keyboard input
- **Dynamic UI**: Adjusts based on content length and user interaction
- **Gesture Processing**: Calculates distances between fingers to detect interactions

## 📋 Performance Tips

- Ensure good lighting conditions for accurate hand tracking
- Use a plain background for better detection
- Position yourself approximately 1-2 feet from the camera
- Keep your hand within the camera's field of view
- For best results, use a 720p or higher resolution webcam

## 🌟 Examples

Check out the `examples/` folder for different implementation examples:

- `basic_usage.py`: Simple implementation of the virtual keyboard

Run the example:
```bash
python examples/basic_usage.py
```

## 🤝 Contributing

We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please read our [Contributing Guidelines](CONTRIBUTING.md) for more details.

## 🐛 Known Issues

- Performance may decrease in low-light conditions
- Rapid typing might not be captured accurately
- Complex backgrounds can reduce tracking accuracy
- Very fast hand movements may not be detected

## 🔮 Future Enhancements

- [ ] Word prediction and auto-complete features
- [ ] Multi-language support
- [ ] Customizable themes and layouts
- [ ] Gesture shortcuts for common actions
- [ ] Mobile device compatibility
- [ ] Voice command integration
- [ ] Training mode for new users
- [ ] Save/load custom layouts

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [CVZone](https://github.com/cvzone/cvzone) for the excellent hand tracking module
- [OpenCV](https://opencv.org/) for computer vision capabilities
- [MediaPipe](https://mediapipe.dev/) for the hand tracking models
- [pynput](https://pypi.org/project/pynput/) for system-level input control

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/your-username/virtual-ai-keyboard/issues) page
2. Create a new issue with detailed information
3. Email us at support@virtualkeyboard.com

## 📊 Version History

- **v1.0.0** (2023-10-15)
  - Initial release
  - Basic virtual keyboard functionality
  - Hand gesture detection
  - Real-time typing feedback

---

<div align="center">

### Made with ❤️ and Python

**Give a ⭐️ if you find this project useful!**

</div>



