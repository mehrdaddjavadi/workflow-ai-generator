# Workflow AI Generator

A powerful Chrome Extension that leverages AI to instantly generate n8n workflow and node JSON configurations. No more manual parameter lookups—just describe what you need, and let AI handle the rest!

**Generate production-ready n8n workflows in seconds using natural language prompts.**

## Overview

Workflow AI Generator is a free, open-source Chrome Extension that bridges the gap between natural language and n8n's JSON configuration format. Whether you're building complex workflows or crafting individual nodes, this extension accelerates your development process by harnessing the power of leading AI models.

### Key Capabilities
- **Multi-AI Support**: Choose from OpenAI GPT, Your local Large Language Models on your machine, Google Gemini, Anthropic Claude, Deepseek, Mistral AI, OpenRouter, Groq, or x.ai (Grok)
- **Bring Your Own Keys**: Use your existing API credits—no subscription fees for the extension
- **Secure & Private**: All API keys stored locally in your browser; never shared with third parties
- **Instant Generation**: Convert natural language descriptions into valid n8n JSON in seconds
- **Generation History**: Keep track of all your previous generations for reference and reuse

## Features

✨ **AI-Powered Generation**
- Describe workflows or nodes in plain English
- Get valid, production-ready JSON output
- Support for complex workflow chains and node parameters

🔑 **Multiple AI Providers**
- OpenAI (GPT-4, GPT-4o-mini)
- Local llms by Ollama
- Deepseek
- Google Gemini (Latest models)
- Anthropic Claude (Claude 3.5 Sonnet)
- Mistral AI
- OpenRouter (Multi-model access)
- Groq (Ultra-fast inference)
- x.ai Grok

🛡️ **Security & Privacy**
- API keys stored exclusively in browser local storage
- No data transmitted to external servers
- Keys only sent directly to respective AI providers
- Transparent, auditable codebase

📱 **Flexible Display Modes**
- Popup window for quick access
- Side panel for dedicated workspace
- Switch modes anytime in settings

📚 **Generation History**
- Access previous generations with timestamps
- Copy and reuse past configurations
- Learn from successful patterns

## Why Workflow AI Generator?

### Speed
Replace hours of manual configuration with seconds of AI generation. Eliminate repetitive node setup and parameter lookups.

### Learning
See how natural language translates into n8n's JSON format. Perfect for understanding node structures and workflow patterns.

### Convenience
Generate JSON right where you work. No need to switch between n8n, documentation, and chat interfaces.

### Cost-Effective
Zero extension fees. Pay only for AI model usage through your provider's account. Use free tier APIs if available.

### Developer-Friendly
- Clean, documented codebase
- Manifest V3 compliant
- Easy to fork and customize
- Active community support

## Installation

### From GitHub (Development/Personal Use)

1. **Clone or Download the Repository**
   ```bash
   git clone https://github.com/mehrdaddjavadi/workflow-ai-generator.git
   cd workflow-ai-generator
   ```

2. **Open Chrome Extensions Dashboard**
   - Open Google Chrome
   - Navigate to `chrome://extensions/`
   - Or: Menu → More Tools → Extensions

3. **Enable Developer Mode**
   - Toggle "Developer mode" in the top-right corner

4. **Load the Extension**
   - Click "Load unpacked"
   - Select the project folder (containing `manifest.json`)
   - The extension will appear in your toolbar

5. **Pin the Extension** (Optional)
   - Click the Extensions icon in your toolbar
   - Click the pin icon next to "Workflow AI Generator"

## Quick Start

### Setup Your AI Provider

1. **Open the Extension** → Click the Workflow AI Generator icon in your toolbar

2. **Navigate to Settings** → Click the "Settings" tab

3. **Enable & Configure an AI Provider:**
   
   **OpenAI (Recommended for GPT-4 quality)**
   - Get API key: [platform.openai.com/api-keys](https://platform.openai.com/api-keys)
   - Paste your key (starts with `sk-...`)
   - Save settings
   - Select your preferred model (e.g., `gpt-4o-mini`)

   **Google Gemini (Free tier available)**
   - Get API key: [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
   - Click "Create API key"
   - Paste into the Gemini field
   - Save settings

   **Anthropic Claude (Excellent reasoning)**
   - Get API key: [console.anthropic.com/keys](https://console.anthropic.com/keys)
   - Paste your key
   - Save settings
   - Select Claude model

   **DeepSeek provides both cloud API access and local runnable models (e.g., via Ollama or custom backends)**
  - Cloud API Setup
      Get your API key:
      https://platform.deepseek.com
      Paste the key into the DeepSeek field. 
      Select a model such as:
      deepseek-chat
      deepseek-reasoner

   **Local Machine LLMs**
      -You can run fully local models without any cloud API. This extension supports Ollama and all of models in local engines.
   **Other Providers**
   - Similar process for Mistral, OpenRouter, Groq, x.ai
   - Refer to provider documentation for API key generation
   DeepSeek (Cloud or Local Variant)
   

4. **Verify Connection** → If valid, models will auto-populate in the dropdown

### Generate Your First Workflow

1. **Click Generate Tab** → Switch to the main "Generate" tab

2. **Select Your AI Provider** → Choose from enabled providers

3. **Write a Prompt** → Be specific and descriptive
   
   **Workflow Example:**
   ```
   Create a workflow that:
   - Triggers daily at 9 AM
   - Fetches user data from https://api.example.com/users
   - Filters for active users only
   - Sends a summary email to admin@example.com
   ```

   **Node Example:**
   ```
   Create an HTTP Request node that:
   - Makes a POST request to https://api.example.com/data
   - Sends JSON body with fields: name, email, timestamp
   - Sets authorization header with Bearer token
   ```

4. **Click "Generate n8n JSON"** → Wait for AI response

5. **Review the Output** → Check JSON for accuracy and correctness

6. **Copy the JSON** → Click the copy button

7. **Paste in n8n** → 
   - Go to your n8n workflow
   - Right-click on canvas → "Paste"
   - Or use `Ctrl+V` / `Cmd+V`

## Security & Privacy

- **Local Storage Only**: API keys never leave your browser's local storage
- **Direct Communication**: Keys only sent directly to AI provider APIs
- **No Tracking**: No telemetry, analytics, or usage tracking
- **Open Source**: Full transparency—review the code yourself
- **Browser Security**: Leverages Chrome's security model

## Important Notes

⚠️ **API Costs**
- You are responsible for all API costs based on your usage
- Monitor your usage on each provider's dashboard
- Consider usage limits and rate limits

⚠️ **JSON Accuracy**
- AI models occasionally make mistakes
- **Always review generated JSON** before pasting into n8n
- Test complex workflows in a sandbox first
- Some parameters may need manual adjustment

⚠️ **Terms of Service**
- Respect each AI provider's terms of service
- Comply with n8n's licensing terms
- Use for personal/development purposes as intended

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Platform**: Chrome Extension Manifest V3
- **Storage**: Chrome Storage API (`chrome.storage.local`)
- **Clipboard**: Chrome Clipboard API (`navigator.clipboard`)
- **API Communication**: Fetch API with proper headers and authentication

## Supported AI Models

| Provider | Models | Free Tier | Best For |
|----------|--------|-----------|----------|
| OpenAI | GPT-4o, GPT-4o-mini, GPT-4 | Limited | Advanced logic, complex workflows |
| Google Gemini | Gemini 1.5 Flash, Pro | Yes | Quick generations, cost-effective |
| Anthropic Claude | Claude 3.5 Sonnet, Opus, Haiku | No | Detailed reasoning, quality outputs |
| Mistral | Mistral-7B, Mistral-Large | No | Fast inference |
| OpenRouter | 100+ Models | Varies | Model variety, comparison testing |
| Groq | LLaMA 2, Mixtral | Limited | Ultra-fast API responses |
| Local LLM | All models on ollama | Yes | Ultra-fast API responses |
| Deepseek | Chat model and reseaning model | No | Ultra-fast API responses |
| x.ai Grok | Grok-1, Grok-2 | No | Experimental, high-performance |

## Troubleshooting

**"No providers enabled in Settings"**
- Go to Settings tab
- Enable at least one AI provider
- Verify API key is entered correctly
- Click Save Settings

**"Model dropdown is empty"**
- Check that your API key is valid
- Verify internet connection
- Try a different provider
- Wait a few seconds and refresh

**"Invalid JSON response"**
- This is an AI error—try a different prompt
- Be more specific in your description
- Try a different AI provider
- Review the output for syntax errors

**"API key error"**
- Double-check your API key (no extra spaces)
- Verify key is active in provider's console
- Check if key has necessary permissions
- Check for rate limiting or quota issues

## Contributing

We welcome contributions! Here's how to get involved:

1. **Report Issues**: Found a bug? [Open an issue](https://github.com/mehrdaddjavadi/workflow-ai-generator/issues)

2. **Suggest Features**: Have an idea? [Start a discussion](https://github.com/mehrdaddjavadi/workflow-ai-generator/discussions)

3. **Submit Code**:
   - Fork the repository
   - Create a feature branch: `git checkout -b feature/YourFeature`
   - Commit your changes: `git commit -am 'Add new feature'`
   - Push to your branch: `git push origin feature/YourFeature`
   - Open a Pull Request with a clear description

4. **Code Standards**:
   - Follow existing code style
   - Add comments for complex logic
   - Test your changes thoroughly
   - Update documentation as needed

## License

This project is licensed under the **MIT License**—free to use, modify, and distribute.

See the [LICENSE](LICENSE) file for full details.

**In short**: You can use this for any purpose, including commercial, but must include the license notice.

## Disclaimer

- This extension is **not affiliated** with n8n, OpenAI, Google, Anthropic, or any AI provider
- **Not officially supported** by n8n or any AI platform
- Use at your own risk—test thoroughly before production use
- We are not responsible for any costs incurred or errors generated

## Support & Community

- **GitHub Issues**: [Report bugs or request features](https://github.com/mehrdaddjavadi/workflow-ai-generator/issues)
- **GitHub Discussions**: [Ask questions, share ideas](https://github.com/mehrdaddjavadi/workflow-ai-generator/discussions)
- **Documentation**: Refer to prompts examples and troubleshooting above

## Credits

**Created by**: Mehrdad Javadi  
**GitHub**: [github.com/mehrdaddjavadi](https://github.com/mehrdaddjavadi)
**Email**:mehrdaddjavadi@gmail.com

**Built with**: Modern JavaScript, Chrome Extension APIs, and AI APIs  
**Inspired by**: The n8n community and AI enthusiasts worldwide

---

**Happy workflow building! 🚀**

Start generating n8n configurations instantly. Focus on your logic, let AI handle the JSON.






