# High-level architecture

```text
                    XANDER (Android app)
                             |
                    Google sign-in
                             |
                  Firebase Realtime Database
               (account / chatbot data stored online)

       User configures a chatbot personality in Xander
                             |
                 Selects an AI provider
                             |
      Groq | Gemini | OpenRouter | Novita | Cohere
                 Hugging Face | Mistral
                             |
        Provider processes prompts and returns replies
```

**Conversation storage note:** Chat history is not saved in Firebase, according to the developer. This document does not claim that chat messages are never processed or retained by the selected AI provider; check that provider's own terms and data controls.

**API key note:** Xander offers limited temporary keys for a quick start, but users are ultimately expected to configure their own provider API key. This repository does not contain API keys. Never commit real secrets, tokens, or credentials.

This is a product-level overview, not a complete implementation diagram. The application's source code is private and is not included in this repository.
