Download full project here: https://drive.google.com/file/d/13BfkQhg90JhOuax264QW60cvmJLloYd_/view?usp=sharing

# AI Lawyer Assistant

A JavaFX desktop assistant that helps draft legal case analysis from text or uploaded documents, then generates clear arguments and counter-arguments.

## Features

- 📝 Case Input: Write a case summary or upload PDF, DOCX, or TXT files
- 🤖 AI Case Analysis: Generate structured arguments, points, and legal reasoning
- 💬 Opposition Reply: Draft counter-arguments against an opposing position
- 🌍 Multi-language Output: Produce analysis in multiple languages
- 📄 Document Parsing: Extracts text from uploaded legal documents
- 💾 Export Ready: Save and share the generated analysis

## Prerequisites

- Java 17 or higher
- Maven 3.6 or higher

## Getting Started

### 1. Clone or navigate to the project directory

```bash
cd c:\Users\nihal\Desktop\major_pro
```

### 2. Configure AI API (Important!)

Open `src/main/java/com/ailawyer/service/AIService.java` and update:

```java
private static final String API_KEY = "YOUR_API_KEY_HERE";
private static final String API_ENDPOINT = "https://api.openai.com/v1/chat/completions";
```

**Supported AI Providers:**
- OpenAI (GPT-4, GPT-3.5)
- Anthropic (Claude)
- Azure OpenAI
- Google AI
- Any OpenAI-compatible API

### 3. Build the project

```bash
mvn clean install
```

### 4. Run the application

```bash
mvn javafx:run
```

## How to Use

1. Select Language: Choose your preferred language from the dropdown
2. Describe Case: Enter case details in the text area
3. Upload Documents (Optional): Add supporting documents (PDF/DOCX/TXT)
4. Analyze Case: Click "Analyze Case" to get AI-generated legal arguments
5. Respond to Opposition (Optional): Enter opposing arguments and get counter-arguments

## Project Structure

```
major_pro/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/ailawyer/
│   │   │       ├── App.java                    # Main application
│   │   │       ├── controller/
│   │   │       │   └── MainController.java      # UI controller
│   │   │       ├── model/
│   │   │       │   └── CaseData.java            # Case data model
│   │   │       └── service/
│   │   │           ├── AIService.java           # AI integration
│   │   │           └── FileParserService.java   # Document parsing
│   │   └── resources/
│   │       ├── fxml/
│   │       │   └── main-view.fxml               # UI layout
│   │       └── css/
│   │           └── styles.css                   # Styling
├── pom.xml                                      # Maven configuration
└── README.md
```

## Technologies Used

- JavaFX: Modern UI framework
- OkHttp: HTTP client for API calls
- Gson: JSON processing
- Apache PDFBox: PDF document parsing
- Apache POI: Word document parsing
- Apache Commons IO**: File handling

## Configuration

### API Configuration

The application uses AI APIs to generate legal analysis. You need to:

1. Get an API key from your chosen provider (OpenAI, Anthropic, etc.)
2. Update `AIService.java` with your credentials
3. Adjust the request format if using a non-OpenAI provider

### Customization

- **Languages**: Add more languages in `MainController.initialize()`
- **AI Model**: Change the model in `AIService.callAI()` method
- **UI Theme**: Modify `styles.css` for different color schemes

## Security Notes

⚠️ **Important Security Considerations:**

- Never commit API keys to version control
- Consider using environment variables or a config file for API keys
- Add `.env` or `config.properties` to `.gitignore`
- Use secure key management in production

## Disclaimer

This application is for educational purposes only. It is not a substitute for professional legal advice. Always consult with a qualified attorney for legal matters.

## Future Enhancements

- [ ] Voice input/output for arguments
- [ ] Case law database integration
- [ ] Multi-case management
- [ ] Collaboration features
- [ ] Advanced document analysis
- [ ] Citation generator
- [ ] Court filing preparation

## License

MIT License - Feel free to use and modify as needed.

## Support

For issues or questions, please create an issue in the project repository.
