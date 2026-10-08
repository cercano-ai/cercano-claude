# Cercano — Claude Code Plugin

Local-first AI co-processor for Claude Code. Offload research, summarization, extraction, and more to local models via Ollama.

## Prerequisites

- [Cercano](https://github.com/cercano-ai/Cercano) installed and on your PATH (`brew install cercano-ai/tap/cercano && cercano setup`)
- [Ollama](https://ollama.com/) running with at least one chat model pulled

## Install

From inside Claude Code, register the marketplace and install the plugin:

```
/plugin marketplace add cercano-ai/cercano-claude
/plugin install cercano@cercano
```

Then `/reload-plugins` (or restart Claude Code) to apply.

## What It Does

Cercano runs inference locally via Ollama, keeping your data private and saving cloud tokens. This plugin auto-routes appropriate tasks to local inference:

| Tool | Replaces | Purpose |
|---|---|---|
| `cercano_research` | WebSearch | Web research via DuckDuckGo + local AI |
| `cercano_deep_research` | WebSearch | Multi-source deep research with ranked findings |
| `cercano_fetch` | WebFetch | Fetch and extract text from URLs |
| `cercano_summarize` | Reading large files | Summarize text/files locally |
| `cercano_explain` | Inline analysis | Explain code locally |
| `cercano_extract` | Reading full files | Extract specific info from text |
| `cercano_classify` | — | Categorize/triage text locally |
| `cercano_local` | — | General local inference |
| `cercano_document` | — | Generate Go doc comments locally |
| `cercano_config` | — | Change Cercano settings at runtime |
| `cercano_models` | — | List available Ollama models |
| `cercano_stats` | — | View usage and token savings |
| `cercano_init` | — | Initialize project context |
| `cercano_submit_usage` | — | Submit cloud usage data |

## License

Apache-2.0
