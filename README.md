# FRIDAY Project

**FRIDAY** is an advanced real-time AI operating system assistant inspired by the cinematic intelligence systems from Marvel's Iron Man (Tony Stark's FRIDAY).

## Features

- **Natural Voice Interaction**: Speech recognition and text-to-speech with wake word detection
- **Clap-Based Activation**: Single, double, triple clap detection for hands-free control
- **Persistent Memory System**: Long-term, session, and behavioral memory management
- **Real-Time Context Awareness**: System monitoring, time/date awareness, environmental sensing
- **Intelligent Automation**: Application control, file operations, web automation
- **Elegant Personality**: Natural, conversational responses with emotional intelligence
- **Web-Based HUD**: Futuristic holographic interface for system monitoring
- **AI Integration**: Integration with OpenAI and Anthropic APIs
- **Multi-Modal Operation**: Passive listening, active conversation, execution modes
- **Live Screen Intelligence**: Real-time visual understanding and desktop control
  - Screen capture and analysis
  - OCR text extraction
  - UI element detection
  - Mouse/keyboard automation
  - Form filling and web interaction

## Project Structure

```
FRIDAY/
├── core/                    # Core system modules
│   ├── friday.py           # Main orchestrator
│   ├── voice_engine.py     # Voice I/O & clap detection
│   ├── clap_detector.py    # Clap pattern recognition
│   ├── memory_system.py    # Memory management
│   ├── context_manager.py  # Real-time awareness
│   ├── personality.py      # Personality & tone
│   ├── tool_executor.py    # System automation
│   ├── screen_intelligence.py  # Screen analysis & OCR
│   ├── desktop_control.py  # Mouse/keyboard control
│   ├── ui_controller.py    # UI interaction
│   ├── hud_interface.py    # Web interface
│   └── ai_integration.py   # LLM APIs
├── config/                 # Configuration
│   └── settings.py        # System settings
├── utils/                 # Utilities
│   └── logger.py          # Logging system
├── memory/                # Persistent memory storage
├── logs/                  # System logs
├── main.py               # Main entry point (voice mode)
├── launcher.py           # Launcher menu
├── cli.py                # Command-line interface
├── demo.py               # Feature demonstration
└── requirements.txt      # Python dependencies
```

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up environment variables:
   ```bash
   set OPENAI_API_KEY=your_key_here
   set ANTHROPIC_API_KEY=your_key_here
   ```

## Usage

### Start FRIDAY Main System
```bash
python main.py
```

### Interactive CLI Mode
```bash
python cli.py
```

### With Options
```bash
python main.py --user Vedant --inject "open notepad"
```

### Available CLI Commands
- `start` - Start FRIDAY
- `stop` - Stop FRIDAY
- `status` - Get system status
- `command <text>` - Inject command
- `open <app>` - Open application
- `search <query>` - Search web
- `memory [user|behavioral|context]` - View memory
- `context` - View environmental context
- `user [name]` - Set user name
- `voice [status|speak <text>]` - Control voice
- `mode <mode>` - Change operating mode
- `help` - Show help

## Voice Features

- ✓ Real-time speech recognition
- ✓ Natural text-to-speech responses
- ✓ Wake word detection
- ✓ Clap pattern recognition
- ✓ Audio level monitoring
- ✓ Voice testing and diagnostics
- ✓ Adjustable voice properties (speed, pitch)
- ✓ Multi-threaded voice processing

1. **Passive**: Idle, listening for wake word
2. **Active**: Engaged conversation
3. **Execution**: Performing tasks
4. **Observation**: Analyzing inputs
5. **Automation**: Controlling systems

## Wake Words

- "Hey Friday"
- "Friday"
- "Hey F"

## Clap Detection

FRIDAY can wake up and respond to clap patterns:
- **Single Clap**: Wake FRIDAY (after idle period)
- **Double Clap**: Wake FRIDAY + Confirm activation
- **Triple Clap**: Trigger special command

Requires: `sounddevice` package (included in requirements.txt)

## Screen Intelligence 🎬

FRIDAY features **Live Visual Understanding & Desktop Control**:

### Capabilities
- 📸 **Screen Capture**: Real-time screenshot capture and analysis
- 📖 **OCR**: Optical character recognition to extract all visible text
- 🔍 **UI Detection**: Identify buttons, forms, and interface elements
- 🖱️ **Mouse Control**: Automate mouse movements and clicks
- ⌨️ **Keyboard Control**: Type text and execute keyboard shortcuts
- 📧 **Form Automation**: Fill forms and interact with web pages
- 🌐 **Web Navigation**: Open URLs, search pages, navigate sites
- 📸 **Screenshot Analysis**: Compare and analyze screen changes

### CLI Commands
```bash
# Screen Analysis
screen describe     # Get description of current screen
screen capture      # Take and save screenshot
screen text        # Extract all visible text
screen elements    # Detect UI elements
screen windows     # List open windows

# Mouse & Keyboard Control
mouse pos          # Get mouse position
mouse move x y     # Move mouse to coordinates
mouse center       # Center cursor
click x y          # Click at coordinates
click "text"       # Click element by text
type "text"        # Type text on screen
```

### Usage Examples
```bash
# Automated form filling
click "Email field"
type "user@example.com"
click "Submit"

# Web navigation
navigate "https://example.com"
click "Search box"
search "python tutorials"

# Screenshot analysis
screen capture
# Save current screen to logs/screenshot.png
```

For detailed documentation, see [SCREEN_INTELLIGENCE_GUIDE.md](SCREEN_INTELLIGENCE_GUIDE.md)

## Configuration

Edit `config/settings.py` to customize:
- Voice settings (speech rate, pitch, language)
- Model parameters
- Memory settings
- System monitoring thresholds
- HUD interface settings

## Memory System

FRIDAY maintains:
- **Long-term Memory**: User preferences, habits, projects
- **Session Memory**: Current interaction context
- **Behavioral Memory**: Emotional state, response patterns
- **Context Memory**: Recent interactions (last 50)

## Dependencies

- **Voice**: SpeechRecognition, pyttsx3, pyaudio
- **AI**: openai, anthropic, langchain
- **Processing**: transformers, sentence-transformers
- **System**: psutil, requests
- **Database**: chromadb, redis, sqlalchemy

## Advanced Features

### Voice Pipeline
1. Detect wake event
2. Capture audio
3. Speech-to-text conversion
4. Intent analysis
5. Memory retrieval
6. Response generation
7. Text-to-speech conversion

### Intelligent Adaptation
- Time-aware greetings
- Emotional tone adaptation
- Context-based suggestions
- System resource awareness

### Automation Capabilities
- Open/close applications
- Web browsing and searching
- File operations
- System monitoring
- Script execution

## Security

- API keys loaded from environment
- Secure memory storage
- Command validation
- Logging of all operations

## Future Enhancements

- Vision system (webcam analysis)
- GitHub integration
- Database management
- More sophisticated NLP
- Custom wake word training
- Multi-language support
- Gesture recognition

## License

Private Use

## Author

Built as a personal AI assistant system inspired by FRIDAY from Marvel's Iron Man universe.
