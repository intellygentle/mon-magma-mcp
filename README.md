
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
npm install dotenv
```
create an env file in your dist folder
``
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
```bash
npx @modelcontextprotocol/inspector /home/username/.nvm/versions/node/v23.11.0/bin/node /home/username/monadMpcTask/dist/monad-magma-Tools.js
```
