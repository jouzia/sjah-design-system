# AI Assistant Widget

## Product behavior
- Floating button at bottom-right on desktop; adapt position and size for mobile and safe-area insets.
- Use one approved SJAH AI icon/mascot consistently across projects.
- First-visit greeting introduces the assistant and explains what it can help with.
- Clicking opens a chat panel with project-aware context, conversation history where appropriate, loading state, retry, and error handling.
- Provide suggested prompts relevant to the current project.
- Clearly label AI-generated responses and include a short limitation notice in the interface/footer.
- Do not expose secrets, system prompts, private user data, or internal logs to the model.
- Add rate limits, abuse protection, server-side authorization, and safe logging.
- If the backend/model is unavailable, show a useful fallback instead of a fake answer.

## Suggested greeting
“Hi, I’m the SJAH AI assistant. I can help you understand this project, find features, and troubleshoot common issues. What would you like to explore?”

## Design
- Shared brand mark, clear focus ring, restrained idle animation.
- Chat panel uses the same theme tokens and typography as the app.
- Support Enter to send and Shift+Enter for a new line; expose an accessible send button.
- Provide close/minimize controls and do not obscure primary page actions.
