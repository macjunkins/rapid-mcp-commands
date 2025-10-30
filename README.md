# Rapid MCP Commands

Shared YAML command definitions for Rapid MCP Server implementations.

## Overview

This repository contains command definitions in YAML format that are consumed by both the Rust and Go implementations of the Rapid MCP Server. By centralizing command definitions, we ensure consistency across implementations.

## Structure

```
rapid-mcp-commands/
├── sanity-check.yaml    # Project health check command
└── [future commands]    # Additional commands will be added here
```

## Command Format

Each YAML file defines a command with the following structure:

```yaml
name: command-name
version: "1.0.0"
description: "Brief description of what the command does"
metadata:
  category: "category-name"
  tags: ["tag1", "tag2"]

parameters:
  - name: param_name
    type: string
    description: "Parameter description"
    required: false
    default: "default-value"

prompt: |
  # Command Template

  Your prompt template goes here with {{parameter}} substitution.
```

## Usage

This repository is referenced by:
- [rapid-mcp-server-rust](https://github.com/macjunkins/rapid-mcp-server-rust) - Rust implementation
- [rapid-mcp-server-go](https://github.com/macjunkins/rapid-mcp-server-go) - Go implementation

Both servers create a symlink to this repository's contents.

## License

MIT License - See individual MCP server repositories for full license details.
