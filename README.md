# Documentation Update Guide

This repo contains the official docs of Hyperleap AI powered by [Mintlify](https://mintlify.com/docs/quickstart).

## File structure

```
├── api-reference/     # Generated API reference tab pages
├── guides/           # Documentation tab pages
├── images/          # Different images used in docs
├── logo/           # Different logos
├── snippets/       # Different snippet components used in pages
├── api.json        # Main API spec file with endpoint related data
├── docs.json       # Main Mintlify configuration file
├── introduction.mdx # Documentation tab introduction file
├── openapi.json    # Studio endpoints OpenAPI spec file (reference)
├── temp.mdx        # Temporary file
└── welcome.mdx     # Welcome page
```

There are 2 main sections (api-reference, general guides)

## API Reference Docs Updates

In the api-reference pages there are 2 kinds: endpoint pages, overview pages

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
   npx @mintlify/scraping@latest openapi-file <path-to-openapi-file> -o <api-reference-folder>

   # Example
   npx @mintlify/scraping@latest openapi-file api.json -o api-reference
   ```

Mintlify **generates or updates** endpoint pages in `<api-reference-folder>` but it **doesnot delete** any existing files in `<api-reference-folder>`

4. Copy the generated array from console to the `API Reference` tab or appropriate tab/group in `docs.json`.
   The output will look like this:

```json
"navigation object suggestion:
[
  {
    "group": "Prompts",
    "pages": [
      "api-reference/prompts/run-prompt-non-streaming",
      "api-reference/prompts/run-prompt-http2-streaming",
      "api-reference/prompts/run-prompt-sse-streaming"
    ]
  },
  {
    "group": "Conversations",
    "pages": [
      "api-reference/conversations/get-all-conversations",
      "api-reference/conversations/create-a-general-conversation",
      "api-reference/conversations/create-a-persona-conversation",
      "api-reference/conversations/get-all-conversations-with-a-persona",
      "api-reference/conversations/get-user-conversations",
      "api-reference/conversations/continue-http2-streaming",
      "api-reference/conversations/continue-sse-streaming",
      "api-reference/conversations/continue-chat",
      "api-reference/conversations/get-specific-conversation",
      "api-reference/conversations/set-conversation-as-active",
      "api-reference/conversations/set-conversations-metadata",
      "api-reference/conversations/set-conversations-name",
      "api-reference/conversations/set-conversations-status"
    ]
  },
  {
    "group": "Capture Feedback",
    "pages": [
      "api-reference/capture-feedback/set-conversation-score",
      "api-reference/capture-feedback/set-messages-score",
      "api-reference/capture-feedback/set-prompt-run-score"
    ]
  },
  {
    "group": "Audit Report",
    "pages": [
      "api-reference/audit-report/conversations",
      "api-reference/audit-report/prompt-runs",
      "api-reference/audit-report/prompt-run-details",
      "api-reference/audit-report/conversation-run-details"
    ]
  },
  {
    "group": "Feedback Report",
    "pages": [
      "api-reference/feedback-report/conversations",
      "api-reference/feedback-report/prompt-runs"
    ]
  },
  {
    "group": "Moderations",
    "pages": [
      "api-reference/moderations/moderations-check"
    ]
  }
]"
```

### Updating Overview Pages

- overview pages are placed in respective folders like `/api-reference/prompts/overview`, `/api-reference/conversations/overview`, `/api-reference/audit-report/overview` etc.
- mintlify does not delete these overview page files when you update api.json and run the scrape command
- Add the overview page reference in respective groups in docs.json under `API Reference` tab

Example: including prompts overview page in prompts group in docs.json

```json
{
                "group": "Prompts",
                "pages": [
                  "api-reference/prompts/overview",  <-----
                  "api-reference/prompts/run-prompt-non-streaming",
                  "api-reference/prompts/run-prompt-http2-streaming",
                  "api-reference/prompts/run-prompt-sse-streaming"
                ]
},
```

## General Docs Updates

- General Docs pages include guides, introduction, welcome, etc.

### Updating Existing Pages

1. Locate the `.mdx` file you want to update, refer docs.json for file path.
2. Make your changes directly in the file
3. Save the file - changes will be reflected automatically

### Creating New Pages

1. Create a new `.mdx` file in the appropriate directory
2. Add your content using [Mintlify components](https://mintlify.com/docs/components/overview)
3. Add the page reference in `docs.json` under the appropriate group/pages section
4. Example page structure:

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

# Troubleshooting

Sometimes AI Code Gens seriously hallucinate and add unneccessary code like `{" "}` when formatting, remove these

## Useful Resources

- [Mintlify Components](https://mintlify.com/docs/components/overview)
- [OpenAPI Documentation](https://mintlify.com/docs/api-playground/openapi/overview)
- [MDX Syntax Guide](https://mintlify.com/docs/writing-content/mdx)

## Need Help?

For more detailed information, visit the [Mintlify Documentation](https://mintlify.com/docs/quickstart).
