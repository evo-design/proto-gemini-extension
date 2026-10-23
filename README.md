# Proto for Gemini CLI

A [Gemini CLI](https://github.com/google-gemini/gemini-cli) extension that connects Gemini to
our hosted MCP server at `https://mcp.evodesign.org/mcp`. It gives Gemini access to Proto's
catalog of generative-biology tools.

## Install

```bash
gemini extensions install https://github.com/evo-design/proto-gemini-extension
```

Start Gemini CLI and run `/mcp auth proto` to sign in to your Proto account. Then run `/mcp` to
confirm that the server is connected.

## Requirements

- A Proto account. Create one at https://proto.evodesign.org/.
- A connected Modal account for GPU tools. Connect it at
  https://proto.evodesign.org/settings/account/modal. Runs are billed to your Modal account.

## Without the extension

You can add the server directly instead:

```bash
gemini mcp add --transport http proto https://mcp.evodesign.org/mcp -s user
```

## Documentation

See https://proto.evodesign.org/docs/mcp/installation.

## License

MIT. See [LICENSE](LICENSE).
