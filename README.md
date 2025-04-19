
### Summary of Commands
Here’s a recap of the prerequisite commands to set up your MCP project:

```bash
git clone
cd
```


# Install dependencies
```bash 
npm isntall
npm install @modelcontextprotocol/sdk zod viem
```
# Build and run
```bash
npm run build
```

# configure claude json file
- copy the output of which node
```bash
which node  # it should look like this /home/yourUsername/.nvm/versions/node/v23.11.0/bin/node
```
- copy the path to your js file
- combine the two to make your claude json setup
- ```bash
  { "mcpServers": {
    "monad-mcp": {
      "command": "wsl",
      "args": [
         "/home/yourUsername/.nvm/versions/node/v23.11.0/bin/node",
        "/home/yourUsername/monadMpcTask/dist/monad-magma-Tools.js"
      ]
    } ```
  


# Test with MCP Inspector
$ npx @modelcontextprotocol/inspector /home/username/.nvm/versions/node/v23.11.0/bin/node /home/username/monadMpcTask/dist/monad-magma-Tools.js
