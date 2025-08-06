# Medical Vision Chatbot

A multimodal AI application that simulates a doctor consultation experience by combining voice input, medical image analysis, and voice output responses.

## Features

- **Voice Input**: Record audio questions using your microphone
- **Image Analysis**: Upload medical images for AI-powered analysis
- **Intelligent Response**: Get medical insights using advanced language models
- **Voice Output**: Receive spoken responses from the AI doctor
- **Interactive Web Interface**: User-friendly Gradio-based interface

## Demo

The application provides a complete consultation workflow:
1. Record your medical question via microphone
2. Upload an image (skin condition, X-ray, etc.)
3. Receive both text and audio responses from the AI doctor

## Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager
- Microphone access for audio recording

### Setup

1. Clone the repository:
```bash
git clone https://github.com/umairs5/medical-vision-chatbot.git
cd ai-doctor-vision-voice
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the root directory and add your API keys:
```env
GROQ_API_KEY=your_groq_api_key_here
ELEVENLABS_API_KEY=your_elevenlabs_api_key_here
```

### Getting API Keys

1. **GROQ API Key**: 
   - Visit [Groq Cloud](https://console.groq.com/)
   - Create an account and generate an API key

2. **ElevenLabs API Key**:
   - Visit [ElevenLabs](https://elevenlabs.io/)
   - Create an account and get your API key from the profile section

## Usage

1. Start the application:
```bash
python gradio_app.py
```

2. Open your web browser and navigate to the displayed local URL (typically `http://127.0.0.1:7860`)

3. Use the interface:
   - Click on the microphone to record your medical question
   - Upload an image for analysis
   - Click submit to get AI doctor's response
   - Listen to the audio response

## Project Structure

```
ai-doctor-vision-voice/
├── gradio_app.py          # Main Gradio application
├── brain.py               # Image analysis and LLM integration
├── voice_patient.py       # Speech-to-text functionality
├── voice_doctor.py        # Text-to-speech functionality
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (create this)
└── README.md             # Project documentation
```

## Models Used

- **Vision**: Meta Llama 4 Scout 17B (via Groq)
- **Speech-to-Text**: Whisper Large v3 (via Groq)
- **Text-to-Speech**: ElevenLabs Turbo v2 with Giovanni voice
- **Fallback TTS**: Google Text-to-Speech (gTTS)

## Important Notes

⚠️ **Disclaimer**: This application is for educational and demonstration purposes only. It should never be used as a substitute for professional medical advice, diagnosis, or treatment. Always consult with qualified healthcare professionals for medical concerns.

## Features in Detail

### Voice Recording
- Automatic ambient noise adjustment
- Configurable timeout and phrase limits
- MP3 format output for compatibility

### Image Analysis
- Support for various medical image formats
- Base64 encoding for secure API transmission
- Contextual analysis based on voice input

### AI Response
- Professional medical tone simulation
- Concise, human-like responses
- Avoids AI-specific language patterns

### Audio Output
- Cross-platform audio playback (Windows, macOS, Linux)
- High-quality voice synthesis
- Automatic file cleanup

## Troubleshooting

### Common Issues

1. **Microphone not working**:
   - Check microphone permissions in your browser
   - Ensure microphone is not being used by other applications

2. **API errors**:
   - Verify your API keys are correct in the `.env` file
   - Check your API usage limits

3. **Audio playback issues**:
   - Install required audio codecs for your operating system
   - Check system audio settings

### System Requirements

- **Windows**: Requires PowerShell or FFmpeg
- **macOS**: Uses built-in `afplay` command
- **Linux**: Requires `aplay` or install `alsa-utils`

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Groq](https://groq.com/) for fast inference capabilities
- [ElevenLabs](https://elevenlabs.io/) for high-quality voice synthesis
- [Gradio](https://gradio.app/) for the intuitive web interface
- [Meta AI](https://ai.meta.com/) for the Llama models

## Support

If you encounter any issues or have questions:
1. Check the troubleshooting section above
2. Search existing issues in the repository
3. Create a new issue with detailed information about your problem

---

**Remember**: This is an educational project. Always seek professional medical advice for real health concerns.
