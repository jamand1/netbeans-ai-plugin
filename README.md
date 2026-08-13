# NetBeans AI Code Generator Plugin

An AI-powered code generation plugin for Apache NetBeans that integrates Google Gemini API to generate code based on natural language prompts.

## Features

- 🤖 **AI Code Generation**: Generate code using natural language prompts powered by Google Gemini
- 🔧 **Seamless Integration**: Panel integrates directly into NetBeans UI
- 📝 **Direct Insertion**: Insert generated code directly into your editor
- 🚀 **Free to Use**: Uses the free Google Gemini API tier

## Installation

### Prerequisites
- Apache NetBeans 15 or later
- Java 11 or later
- Maven 3.6 or later

### Build Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/jamand1/netbeans-ai-plugin.git
   cd netbeans-ai-plugin
   ```

2. Build the plugin:
   ```bash
   mvn clean package
   ```

3. The plugin NBM file will be generated at: `target/netbeans-ai-plugin-1.0.0.nbm`

4. Install in NetBeans:
   - Open NetBeans
   - Go to **Tools → Plugins**
   - Click **"Downloaded"** tab
   - Click **"Add Plugins..."**
   - Select the generated `.nbm` file
   - Click **"Install"**
   - Restart NetBeans

## Usage

1. After installation, go to **Tools → Show AI Code Generator**
2. A panel will appear on the right side of your editor
3. Enter your code prompt (e.g., "Create a Java function to calculate fibonacci")
4. Click **"Generate Code"**
5. Review the generated code
6. Click **"Insert into Editor"** to insert it into your current file at the cursor position

## Configuration

The plugin comes with a pre-configured Google Gemini API key. If you want to use your own:

1. Get your API key from: https://aistudio.google.com/app/apikey
2. Open `src/main/java/com/jamand1/netbeans/ai/plugin/ui/AIGeneratorTopComponent.java`
3. Replace the `API_KEY` constant with your own key
4. Rebuild the plugin

## Project Structure

```
.
├── pom.xml                                    # Maven configuration
├── src/
│   └── main/
│       ├── java/com/jamand1/netbeans/ai/plugin/
│       │   ├── GeminiAPIClient.java          # Gemini API client
│       │   ├── actions/
│       │   │   └── AICodeGeneratorAction.java # Menu action
│       │   └── ui/
│       │       └── AIGeneratorTopComponent.java # UI Panel
│       ├── nbm/
│       │   └── manifest.mf                   # NetBeans module manifest
│       └── resources/
│           └── com/jamand1/netbeans/ai/plugin/
│               ├── Bundle.properties          # Localization
│               └── layer.xml                  # UI configuration
└── README.md
```

## Dependencies

- Apache NetBeans API
- Jackson (JSON processing)
- Google Guava

## License

MIT License

## Author

Jamie Anderson (jamand1)
