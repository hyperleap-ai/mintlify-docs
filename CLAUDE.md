# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is Hyperleap AI's documentation site built with Mintlify. It serves as comprehensive documentation for an AI platform offering prompts, conversations, personas, tools, assistants, and chatbots.

## Key Commands

**Regenerate API Reference Documentation:**
```bash
npx @mintlify/scraping@latest openapi-file api.json -o api-reference
```
Run this after updating `api.json` to regenerate API reference pages.

## Architecture

### Configuration-Driven Structure
- `docs.json` - Primary Mintlify configuration controlling navigation, theming, and site structure
- `api.json` - OpenAPI specification for main API endpoints
- `openapi.json` - Studio endpoints OpenAPI spec (reference only)

### Content Organization
- `/guides/` - User-facing documentation organized by feature (chatbots, prompts, personas, tools, assistants)
- `/api-reference/` - Auto-generated API documentation from OpenAPI specs
- `/snippets/` - Reusable MDX components and shared content
- `/images/` - Assets organized by feature with descriptive subfolder structure

### Documentation Workflow
1. **API Documentation**: Update `api.json` → run scraping command → update navigation in `docs.json`
2. **Overview Pages**: Manually created MDX files (not auto-generated)
3. **User Guides**: Direct editing of MDX files with YAML frontmatter

## Content Standards

- Use MDX format with YAML frontmatter for all documentation
- Remove AI-generated formatting artifacts like `{" "}` when editing
- Maintain consistent image naming and organization within feature subfolders
- Keep navigation structure in `docs.json` synchronized with actual file structure