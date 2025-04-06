This is an outline for an app with live voice-to-voice conversational AI that can function call to an image analysis module and maintain interaction with the user about the image. It is a conversational live multimodal art tutor. ⁠

We will be using DeepGram a Voice Agent for the voice-to-voice conversational AI. Here is the documentation. Please refer to it for details and instructions. 

developers.deepgram.com/docs/voice-agent


[The image analyis component to be used by the Voice Agent](image_analysis_module)

https://developers.deepgram.com/docs/voice-agent
https://developers.deepgram.com/docs/voice-agent-feature-overview
https://developers.deepgram.com/docs/voice-agent-starter-apps
https://developers.deepgram.com/docs/configure-voice-agent
https://developers.deepgram.com/docs/voice-agents-function-calling
https://developers.deepgram.com/docs/build-a-function-call
https://developers.deepgram.com/docs/voice-agent-inputs
https://developers.deepgram.com/docs/voice-agent-settings-configuration
https://developers.deepgram.com/docs/voice-agent-update-instructions
https://developers.deepgram.com/docs/voice-agent-update-speak
https://developers.deepgram.com/docs/voice-agent-inject-agent-message
https://developers.deepgram.com/docs/voice-agent-function-call-response
https://developers.deepgram.com/docs/agent-keep-alive
https://developers.deepgram.com/docs/voice-agent-outputs
https://developers.deepgram.com/docs/voice-agent-welcome-message
https://developers.deepgram.com/docs/voice-agent-setting-applied-message
https://developers.deepgram.com/docs/voice-agent-conversation-text
https://developers.deepgram.com/docs/voice-agent-user-started-speaking
https://developers.deepgram.com/docs/voice-agent-agent-thinking
https://developers.deepgram.com/docs/voice-agent-function-call-request
https://developers.deepgram.com/docs/voice-agent-function-calling-message
https://developers.deepgram.com/docs/voice-agent-agent-started-speaking
https://developers.deepgram.com/docs/voice-agent-agent-audio-done
https://developers.deepgram.com/docs/voice-agent-server-errors
https://developers.deepgram.com/docs/voice-agent-llm-models
https://developers.deepgram.com/docs/voice-agent-media-inputs-outputs
https://developers.deepgram.com/docs/voice-agent-audio-playback
https://developers.deepgram.com/docs/voice-agent-echo-cancellation

## Documentation Summaries

*   **Getting Started:** (developers.deepgram.com/docs/voice-agent) - Initial guide on connecting via WebSocket, sending audio, receiving agent speech, and exchanging messages using an API Key.
*   **Feature Overview:** (developers.deepgram.com/docs/voice-agent-feature-overview) - High-level matrix of features: voice selection, supported LLMs, input/output messages, rate limits.
*   **Starter Apps:** (developers.deepgram.com/docs/voice-agent-starter-apps) - Links to ready-made demo applications (Node.js, Flask with function calling).
*   **Configure the Voice Agent:** (developers.deepgram.com/docs/configure-voice-agent) - Configuration (agent behavior, audio) is done via a `Settings Configuration` message post-connection.
*   **Function Calling (Concept):** (developers.deepgram.com/docs/voice-agents-function-calling) - LLM's ability to invoke external code (APIs, functions) based on conversation context.
*   **Build A Function Call:** (developers.deepgram.com/docs/build-a-function-call) - Guide to building function calls, referencing a Flask example repo.
*   **Inputs: Client Messages:** (developers.deepgram.com/docs/voice-agent-inputs) - Client sends JSON commands to control the agent, configure settings, or provide info (like function call results).
*   **Settings Configuration:** (developers.deepgram.com/docs/voice-agent-settings-configuration) - Details the initial JSON message (`SettingsConfiguration`) for setting agent behavior (LLM, instructions, voice) and audio formats.
*   **Update Instructions:** (developers.deepgram.com/docs/voice-agent-update-instructions) - `UpdateInstructions` message allows modifying agent instructions mid-conversation.
*   **Update Speak:** (developers.deepgram.com/docs/voice-agent-update-speak) - `UpdateSpeak` message changes the agent's TTS voice model mid-conversation.
*   **Inject Agent Message:** (developers.deepgram.com/docs/voice-agent-inject-agent-message) - `InjectAgentMessage` command makes the agent speak immediately (e.g., status updates, prompts).
*   **Function Call Response:** (developers.deepgram.com/docs/voice-agent-function-call-response) - Client *must* send `FunctionCallResponse` with results after executing an agent-requested function.
*   **Agent Keep Alive:** (developers.deepgram.com/docs/agent-keep-alive) - `KeepAlive` message prevents connection closure due to inactivity (often unneeded with continuous mic input).
*   **Outputs: Server Events:** (developers.deepgram.com/docs/voice-agent-outputs) - Server sends messages about conversation status (user speaking, agent thinking, function requests).
*   **Welcome:** (developers.deepgram.com/docs/voice-agent-welcome-message) - `Welcome` message confirms successful WebSocket connection.
*   **Settings Applied:** (developers.deepgram.com/docs/voice-agent-setting-applied-message) - `SettingsApplied` confirms server received and applied initial client `SettingsConfiguration`.
*   **Conversation Text:** (developers.deepgram.com/docs/voice-agent-conversation-text) - `ConversationText` relays transcribed text from both user and agent speech.
*   **User Started Speaking:** (developers.deepgram.com/docs/voice-agent-user-started-speaking) - Event notifies when the user begins speaking.
*   **Agent Thinking:** (developers.deepgram.com/docs/voice-agent-agent-thinking) - Event indicates the agent (LLM) is processing or formulating a response.
*   **Function Call Request:** (developers.deepgram.com/docs/voice-agent-function-call-request) - Message sent when the LLM decides to invoke a client-defined external function.
*   **Function Calling Message:** (developers.deepgram.com/docs/voice-agent-function-calling-message) - Provides debugging insights related to the function call workflow.
*   **Agent Started Speaking:** (developers.deepgram.com/docs/voice-agent-agent-started-speaking) - Event signals the server is starting to stream agent audio response.
*   **Agent Audio Done:** (developers.deepgram.com/docs/voice-agent-agent-audio-done) - Message signals the server finished sending the last audio chunk for the current response.
*   **Agent Server Errors:** (developers.deepgram.com/docs/voice-agent-server-errors) - `Error` message is sent if an issue occurs on the server side.
*   **LLM Models:** (developers.deepgram.com/docs/voice-agent-llm-models) - Explains defining the LLM provider/model in `SettingsConfiguration`.
*   **Media Inputs & Outputs:** (developers.deepgram.com/docs/voice-agent-media-inputs-outputs) - Details configuring audio input (STT encoding/rate) and output (TTS container/encoding/voice) settings.
*   **Voice Agent Audio & Playback:** (developers.deepgram.com/docs/voice-agent-audio-playback) - Troubleshooting tips for audio issues (static, browser playback, self-triggering).
*   **Voice Agent Echo Cancellation:** (developers.deepgram.com/docs/voice-agent-echo-cancellation) - Describes Adaptive Echo Cancellation (AEC) to prevent agent audio feedback loop.