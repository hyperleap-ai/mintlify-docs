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

# Documentation Update Guide

This repository contains the official documentation powered by [Mintlify](https://mintlify.com/docs/quickstart). Below is a guide on how to update different parts of the documentation.

## API Documentation Updates

### Updating API Endpoints

1. Open `api.json` in the root directory
2. Add/modify endpoint information in OpenAPI format with:

   - Proper tags
   - Summary
   - Description
   - Request/Response schemas
   - Parameters
   - HTTP methods (GET, POST, PATCH, etc.)

3. After updating `api.json`, run:

   ```bash
   # Reference format
   npx @mintlify/scraping@latest openapi-file <path-to-openapi-file> -o api-reference

   # Example with our api.json
   npx @mintlify/scraping@latest openapi-file api.json -o api-ref
   ```

4. Copy the generated navigation object from console to the appropriate tab/group in `docs.json`. The output will look like this:

   ```json
   "navigation object suggestion:
   [
     {
       "group": "Prompts",
       "pages": [
         "api-ref/prompts/run-prompt-non-streaming",
         "api-refe/prompts/run-prompt-http2-streaming",
         "api-refe/prompts/run-prompt-sse-streaming"
       ]
     },
     {
       "group": "Conversations",
       "pages": [
         "api-refe/conversations/get-all-conversations",
         "api-refe/conversations/create-a-general-conversation",
         "api-refe/conversations/create-a-persona-conversation",
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
   ]"
   ```

   Use this generated structure to update the navigation in your `docs.json` file.

## General Documentation Updates

### Updating Existing Pages

1. Locate the `.mdx` file you want to update
2. Make your changes directly in the file
3. Save the file - changes will be reflected automatically

### Creating New Pages

1. Create a new `.mdx` file in the appropriate directory
2. Add your content using [Mintlify components](https://mintlify.com/docs/components/overview)
3. Add the page reference in `docs.json` under the appropriate group/section
4. Example structure:

   ```mdx
   ---
   title: "Page Title"
   description: "Page Description"
   ---

   Your content here
   ```

### Removing Pages

1. Remove the page reference from `docs.json`
2. Optionally delete the `.mdx` file (or keep for future use)

## Useful Resources

- [Mintlify Components](https://mintlify.com/docs/components/overview)
- [OpenAPI Documentation](https://mintlify.com/docs/api-playground/openapi/overview)
- [MDX Syntax Guide](https://mintlify.com/docs/writing-content/mdx)

## Need Help?

For more detailed information, visit the [Mintlify Documentation](https://mintlify.com/docs/quickstart).
