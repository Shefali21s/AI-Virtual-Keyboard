# AI-Virtual-Keyboard

A gesture-based virtual keyboard that allows you to type using hand gestures captured via webcam. This innovative application uses computer vision to detect finger movements and translates them into keyboard inputs.

## Features

- **Touchless Typing**: Type without physical contact using hand gestures
- **Real-Time Hand Tracking**: Accurate detection of 21 hand landmarks
- **Dynamic Text Display**: Auto-expanding text area with word wrapping
- **Visual Feedback**: Clear indicators for key activation and shift status
- **Full Keyboard Functionality**: Support for letters, punctuation, and special keys
- **Cross-Platform**: Works on Windows, macOS, and Linux

## Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/virtual-ai-keyboard.git
cd virtual-ai-keyboard
Install the required dependencies:

bash
Copy
Download
pip install -r requirements.txt
Usage
Run the application:

bash
Copy
Download
python main.py
Position your hand in view of the webcam

Move your index finger over the desired key

Pinch your thumb and index finger together to "press" the key

Use the special keys:

Shift: Toggle uppercase characters

Space: Insert space

Ent: Enter key

Bac: Backspace

Clear: Clear all text

Keyboard Layout
The virtual keyboard follows this layout:

text
Copy
Download
Q   W   E   R   T   Y   U   I   O   F
A   S   D   F   G   H   J   K   L   ;
Shift  Z   X   C   V   B   N   M   ,   .
Space  Ent  Bac  Clear
Customization
You can easily customize the keyboard by modifying the KEYBOARD_LAYOUT array in main.py:

python
Copy
Download
KEYBOARD_LAYOUT = [
    ["Q", "W", "E", "R", "T", "Y", "U", "I", "O", "P"],
    ["A", "S", "D", "F", "G", "H", "J", "K", "L", ";"],
    ["Shift", "Z", "X", "C", "V", "B", "N", "M", ",", "."],
    ["Space", "Ent", "Bac", "Clear"]
]
Adjust detection sensitivity by changing these parameters:

python
Copy
Download
self.detector = HandDetector(detectionCon=0.7, maxHands=1)  # Lower = more sensitive
length < 45  # Increase for easier activation
Performance Tips
Ensure good lighting conditions for accurate hand tracking

Use a plain background for better detection

Position yourself approximately 1-2 feet from the camera

Keep your hand within the camera's field of view

Examples
Check out the examples/ folder for different implementation examples:

basic_usage.py: Simple implementation of the virtual keyboard

Known Issues
Performance may decrease in low-light conditions

Rapid typing might not be captured accurately

Complex backgrounds can reduce tracking accuracy

Future Enhancements
Word prediction and auto-complete features

Multi-language support

Customizable themes and layouts

Gesture shortcuts for common actions

Mobile device compatibility

Contributing
We welcome contributions! Please feel free to submit issues, feature requests, or pull requests.

Fork the repository

Create your feature branch (git checkout -b feature/amazing-feature)

Commit your changes (git commit -m 'Add some amazing feature')

Push to the branch (git push origin feature/amazing-feature)

Open a Pull Request

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
CVZone for the hand tracking module

OpenCV for computer vision capabilities

pynput for system-level input control

Support
If you encounter any issues or have questions:

Check the Issues page

Create a new issue with detailed information
