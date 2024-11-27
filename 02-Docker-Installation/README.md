# Docker Installation

## Docker Installations

- **Docker Official Installations Guide**: [Docker Install](https://docs.docker.com/install/)

### Docker Desktop on Windows
- Official Docker Desktop installation for Windows: [Docker Desktop on Windows](https://docs.docker.com/docker-for-windows/)

### Docker Desktop on Mac
- Official Docker Desktop installation for Mac: [Docker Desktop on MAC](https://docs.docker.com/docker-for-mac/)

### Troubleshooting Docker Desktop Issues on Mac

Docker Desktop on Mac has an issue with the macOS keychain (`osxkeychain`). To fix this, follow the steps below:

#### Pre-requisite
For additional understanding, refer to this link:
- [Error creating Docker image on macOS (WSO2 Enterprise Integrator Tooling)](https://medium.com/@dakshika/error-creating-the-docker-image-on-macos-wso2-enterprise-integrator-tooling-dfb5b537b44e)

#### Step 1: Docker Desktop Changes
1. Open **Docker Desktop**.
2. Navigate to **Preferences**.
3. Uncheck the option named **Securely store Docker logins in macOS keychain**.

#### Step 2: Modify `config.json` File in the `.docker` Folder
1. Locate the `config.json` file in the `.docker` folder.  
   Sample reference location:  
   `/Users/<your-username>/.docker/config.json`  
   or  
   `~/.docker/config.json`
2. Open the `config.json` file and remove the line:
   ```json
   "credsStore": "osxkeychain"
