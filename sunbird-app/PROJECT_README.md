# Sunbird AI local Language Assistant

This application is a generative AI tool powered by **Sunbird AI**. it allows users to provide either text or an audio file, which is then summarized, translated into a local Ugandan language, and converted back into speech.

## 🚀 Architecture Overview
The application follows a linear pipeline:
1. **Input**: User provides text or uploads an audio file (max 5 minutes).
2. **STT (Speech-to-Text)**: If audio is provided, it is transcribed to English text.
3. **Summarization**: The English text is summarized using the Sunflower LLM.
4. **Translation**: The summary is translated into a chosen local language (Luganda, Runyankole, Ateso, Lugbara, or Acholi).
5. **TTS (Text-to-Speech)**: The translated summary is converted into an audio clip.
6. **Output**: The UI displays all intermediate steps and a playable audio file.

## 🛠️ Local Setup

1. **Clone the repository**:
   ```bash
   git clone <your-repo-url>
   cd internship-assessment/sunbird-app
   ```

2. **Set up Virtual Environment**:
   ```bash
   python -m venv venv
   # Windows
   .\venv\Scripts\Activate.ps1
   # Linux/Mac
   source venv/bin/activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables**:
   Create a `.env` file in the `sunbird-app` folder and add your Sunbird API Token:
   ```env
   SUNBIRD_API_TOKEN=your_token_here
   ```

5. **Run the App**:
   ```bash
   streamlit run app.py
   ```

## 🔑 Environment Variables
| Variable | Description |
| --- | --- |
| `SUNBIRD_API_TOKEN` | Your unique API token from the Sunbird AI Portal. |

## ⚠️ Known Limitations
- Audio files are limited to 5 minutes for processing.
- Requires an active internet connection to communicate with Sunbird AI APIs.
SUNBIRD_API_TOKEN=your_sunbird_api_token_here
