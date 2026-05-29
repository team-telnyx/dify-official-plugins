# Telnyx Model Provider

This plugin adds Telnyx AI model support for Dify.

## Source repository

The plugin source is maintained at:

https://github.com/team-telnyx/dify-official-plugins/tree/feat/telnyx-model-provider/models/telnyx

## Supported capabilities

- LLM/chat completions via `POST /v2/ai/chat/completions`
- Text embeddings via `POST /v2/ai/openai/embeddings`
- Text-to-speech via `POST /v2/text-to-speech/speech`
- Speech-to-text via `POST /v2/ai/audio/transcriptions`

The predefined model YAML files are aligned with Telnyx's official docs and the live `/v2/ai/openai/models` and `/v2/ai/openai/embeddings/models` model-list endpoints.

## Requirements

- A Dify instance that supports model provider plugins.
- A Telnyx account with access to Telnyx AI APIs.
- A Telnyx API key. Create or manage API keys in the Telnyx Portal: https://portal.telnyx.com/#/app/api-keys
- Network access from your Dify deployment to `https://api.telnyx.com` unless you configure a compatible proxy.

## Setup

1. Install the plugin from Dify Marketplace, or upload the packaged `.difypkg` in the Dify plugin management UI.
2. Open the Telnyx model provider settings in Dify.
3. Enter your Telnyx API key in `telnyx_api_key`.
4. Leave `telnyx_api_base` set to `https://api.telnyx.com` for normal Telnyx usage. Override it only when using a compatible proxy that implements the same Telnyx API paths.
5. Optionally set `validate_model` to a Telnyx embedding model name such as `thenlper/gte-large` when validating provider-level credentials.
6. Save the provider configuration and enable the desired Telnyx models in Dify.

## Usage

After setup, choose Telnyx models anywhere Dify accepts a model provider:

- Use Telnyx chat models in chatflows, workflows, and agents for LLM inference.
- Use Telnyx embedding models for dataset indexing or retrieval workflows.
- Use Telnyx speech-to-text for audio transcription.
- Use Telnyx text-to-speech for voice/audio generation.

Prompts, text, and audio passed to these models are sent to Telnyx APIs for inference, transcription, or synthesis using the configured Telnyx credentials.
