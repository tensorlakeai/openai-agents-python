# Filesystem MCP example tools

Use Node.js 22+ and pnpm 11.28.5. Install the locked example tools from the
repository root:

```sh
npm install --global --ignore-scripts pnpm@11.28.5
pnpm --dir examples/mcp install --frozen-lockfile --ignore-scripts
```

The filesystem, tool-filter and get-all-tools examples launch the installed
executable directly. They do not download a package when starting the server.
The tools project requires a strict 24-hour registry release delay, publication
timestamps and disabled installation hooks; frozen locks are rechecked.
Running an example without the installed executable fails with setup guidance.
Other examples can still use the supported generic MCPServerStdio command API.
