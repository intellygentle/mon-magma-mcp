### Summary of Commands
Here’s a recap of the prerequisite commands to set up your MCP project:

```bash
git clone https://github.com/intellygentle/mon-magma-mcp.git
cd mon-magma-mcp
```


# Install dependencies
```bash 
npm isntall
npm install @modelcontextprotocol/sdk zod viem
npm install dotenv
```
- create an env file in your dist folder
  ```bash
  code .env # fill it with PRIVATE_KEY=0xYourPrivateKey
  ```

- edit the monad-magma-Tools.ts in the src folder with the path to your env. this is so that claude can load it

<img width="374" alt="env" src="https://github.com/user-attachments/assets/71bf86af-f7e0-449c-9620-b50e88ce3acc" />

 
# Build and run
```bash
npm run build
```
run the script
```bash
node dist/monad-magma-Tools.js
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
    }
  ```

# Test with MCP Inspector
be sure to edit "username" use your directory
```bash
npx @modelcontextprotocol/inspector /home/username/.nvm/versions/node/v23.11.0/bin/node /home/username/monadMpcTask/dist/monad-magma-Tools.js
```

# MCP Inspector will look like this
<img width="953" alt="image" src="https://github.com/user-attachments/assets/7ee3f894-1a30-45c7-a5c3-17bfc9a49d57" />

# Claude will look like this
<img width="628" alt="Screenshot 2025-04-19 070802" src="https://github.com/user-attachments/assets/44ab9d8b-ae03-4c0d-9e7e-6a0bd386003b" />
<img width="820" alt="stakemcp" src="https://github.com/user-attachments/assets/7cb080e7-f8c1-4103-8fdc-ece53763a8a5" />


