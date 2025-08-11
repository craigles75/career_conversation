# Career Conversation Chatbot

A personalized AI chatbot that represents Craig Penfold and can answer questions about his career, background, skills, and experience. Built with OpenAI's GPT-4 and Gradio for a web-based chat interface.

## Features

- **Personalized Responses**: The chatbot acts as Craig Penfold, answering questions about his professional background
- **Career Information**: Access to LinkedIn profile and personal summary for accurate responses
- **User Engagement Tracking**: Records interested users and their contact information
- **Question Logging**: Tracks questions that couldn't be answered for continuous improvement
- **Sports Enthusiasm**: Special responses for Cronulla Sharks and Sydney Swans fans
- **Web Interface**: Clean, user-friendly chat interface built with Gradio

## Prerequisites

- Python 3.12 or higher
- OpenAI API key
- Pushover account (for notifications)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd career_conversation
```

2. Install dependencies using uv (recommended):
```bash
uv sync
```

Or using pip:
```bash
pip install -r requirements.txt
```

3. Set up environment variables:
Create a `.env` file in the project root with:
```env
OPENAI_API_KEY=your_openai_api_key_here
PUSHOVER_TOKEN=your_pushover_token_here
PUSHOVER_USER=your_pushover_user_id_here
```

## Usage

1. Ensure your personal information is set up:
   - Place your LinkedIn profile PDF in `me/linkedin.pdf`
   - Update your personal summary in `me/summary.txt`

2. Run the application:
```bash
python main.py
```

3. Open your browser and navigate to the local URL displayed in the terminal (typically `http://localhost:7860`)

4. Start chatting! The bot will respond as Craig Penfold, answering questions about your career and background.

## Project Structure

```
career_conversation/
├── main.py              # Main application file
├── me/
│   ├── linkedin.pdf     # LinkedIn profile PDF
│   └── summary.txt      # Personal background summary
├── requirements.txt      # Python dependencies
├── pyproject.toml       # Project configuration
└── README.md           # This file
```

## Key Components

### Me Class
The core class that handles:
- Loading personal information from PDF and text files
- Managing OpenAI API interactions
- Processing tool calls for user tracking
- Generating system prompts for the AI

### Tool Functions
- `record_user_details`: Captures interested users' contact information
- `record_unknown_question`: Logs questions that couldn't be answered

### Chat Interface
Built with Gradio, providing a clean web-based chat experience that integrates seamlessly with the AI backend.

## Configuration

The chatbot is configured through several mechanisms:

1. **Environment Variables**: API keys and notification settings
2. **Personal Files**: LinkedIn profile and summary text
3. **System Prompt**: Customizable personality and response guidelines
4. **Tool Definitions**: JSON schemas for function calling

## Dependencies

- **openai**: OpenAI API client for GPT-4 integration
- **gradio**: Web interface framework
- **pypdf**: PDF text extraction
- **python-dotenv**: Environment variable management
- **requests**: HTTP client for notifications

## Contributing

This is a personal project, but suggestions for improvements are welcome. The code is structured to be easily customizable for other professionals who want to create their own career conversation bot.

## License

[Add your license information here]

## Support

For questions or issues, please contact Craig Penfold or create an issue in the repository.
