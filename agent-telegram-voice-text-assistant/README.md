Telegram AI Personal Assistant (n8n Workflow)


📌 Overview

This n8n workflow is a powerful AI personal assistant connected to Telegram. It supports both text and voice input and text and voice output, making it a highly interactive and flexible chatbot. It utilizes OpenAI for transcription, response generation, and text-to-speech (TTS) synthesis.


🔥 Features

📩 Text & Voice Input: Users can send text messages or voice recordings via Telegram.

📝 Speech-to-Text (STT): Uses OpenAI Whisper to transcribe audio messages.

🤖 AI Agent: Processes user input through an AI model (ChatGPT or custom LLMs via OpenAI API).

🔄 Memory Buffer: Maintains context for dynamic and coherent conversations.

🔊 Text-to-Speech (TTS): Converts AI-generated responses to voice messages.

📤 Text & Voice Output: Sends responses back as text messages or audio replies, depending on user preference.

🏗️ Workflow Breakdown

Telegram Trigger – Captures incoming messages (text or voice).

Switch Node – Identifies whether the input is text or audio.

GetAudio (if voice message) – Downloads the voice recording.

OpenAI STT – Converts the voice message to text.

AI Agent (OpenAI ChatGPT/LLM) – Processes user queries with memory support.

If Node – Checks if the response should be in text or voice.

Generate Audio (TTS, if voice output is preferred) – Converts text response into an audio file.

Send Message via Telegram – Sends back either a text or voice response.
