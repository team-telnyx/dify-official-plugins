# Privacy Policy

The Telnyx model provider plugin connects Dify to Telnyx AI APIs using credentials configured by the Dify workspace administrator.

## Data processed

Depending on which capability is used, the plugin sends the following data to Telnyx APIs for processing:

- User prompts, chat messages, and model parameters for LLM/chat completion requests.
- Input text for embedding requests.
- Input text for text-to-speech synthesis requests.
- Audio files and related transcription parameters for speech-to-text requests.
- Provider configuration values required to call Telnyx APIs, including the configured Telnyx API key and optional API base URL.

## Storage

The plugin itself does not persist user prompts, text, audio, generated outputs, or personal data outside of Dify. Dify may store workflow inputs, outputs, logs, or configuration according to your Dify deployment settings. Telnyx may process and retain data according to Telnyx's applicable terms and privacy policy.

## Third-party processing

Data sent through this plugin is processed by Telnyx to provide inference, transcription, synthesis, and embedding services. Review Telnyx's privacy policy before enabling this plugin:

https://telnyx.com/privacy-policy