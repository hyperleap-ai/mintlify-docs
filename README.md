# Hyperleap Documentation

Welcome to the official documentation for Hyperleap. This documentation will help you understand and integrate with our platform.

## Getting Started

Hyperleap provides powerful AI capabilities through a simple API. Whether you're building conversational interfaces, analyzing text, or creating AI-powered applications, our platform makes it easy to integrate advanced AI features into your products.

### Key Features

- **Conversational AI**: Create and manage AI conversations with customizable personas
- **Prompt Engineering**: Run prompts with various streaming options
- **Feedback Collection**: Capture and analyze user feedback on AI interactions
- **Audit Capabilities**: Comprehensive audit reports for conversations and prompt runs
- **Moderation**: Content moderation tools to ensure safe AI interactions

## Authentication

All API requests require authentication using an API key. You can obtain your API key from the [Hyperleap Dashboard](https://studio.hyperleapai.com).

Include your API key in the header of all requests:

```
Authorization: Bearer YOUR_API_KEY
```

## Next Steps

- Explore our [API Reference](/api-reference) for detailed endpoint documentation
- Check out our [Guides](/guides/faq) for common questions and troubleshooting
- Visit our [website](https://hyperleapai.com) for more information about Hyperleap

For support, please contact us at [gopi@hyperleap.ai](mailto:gopi@hyperleap.ai).



-----------

      {
        "tab": "API Reference",
        "groups": [
          {
            "group": "Prompts",
            "pages": [
              "api-ref/prompts/run-prompt-non-streaming",
              "api-ref/prompts/run-prompt-http2-streaming",
              "api-ref/prompts/run-prompt-sse-streaming"
            ]
          },
          {
            "group": "Conversations",
            "pages": [
              "api-ref/conversations/get-all-conversations",
              "api-ref/conversations/create-a-general-conversation",
              "api-ref/conversations/create-a-persona-conversation",
              "api-ref/conversations/get-all-conversations-with-a-persona",
              "api-ref/conversations/get-user-conversations",
              "api-ref/conversations/continue-http2-streaming",
              "api-ref/conversations/continue-sse-streaming",
              "api-ref/conversations/continue-chat",
              "api-ref/conversations/get-specific-conversation",
              "api-ref/conversations/set-conversation-as-active",
              "api-ref/conversations/set-conversations-metadata",
              "api-ref/conversations/set-conversations-name",
              "api-ref/conversations/set-conversations-status"
            ]
          },
          {
            "group": "Capture Feedback",
            "pages": [
              "api-ref/capture-feedback/set-conversation-score",
              "api-ref/capture-feedback/set-messages-score",
              "api-ref/capture-feedback/set-prompt-run-score"
            ]
          },
          {
            "group": "Audit Report",
            "pages": [
              "api-ref/audit-report/conversations",
              "api-ref/audit-report/prompt-runs",
              "api-ref/audit-report/prompt-run-details",
              "api-ref/audit-report/conversation-run-details"
            ]
          },
          {
            "group": "Feedback Report",
            "pages": [
              "api-ref/feedback-report/conversations",
              "api-ref/feedback-report/prompt-runs"
            ]
          },
          {
            "group": "Moderations",
            "pages": [
              "api-ref/moderations/moderations-check"
            ]
          }
        ]
      }



        "groups": [
          {
            "group": "Guides",
            "pages": ["guides/faq", "guides/troubleshooting", "guides/error-codes"]
          }
        ]