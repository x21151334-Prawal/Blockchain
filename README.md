
Metamask

The Metamask plugin has been setup in the browser Chrome.
- Step 1: Go to Chrome Extension webstore and search for Metamask. https://chrome.google.com/webstore/category/extensions?utm_source=chrome-ntp-icon
- Step 2: Install the Metamask extension and add it to the menu bar of Chrome
- Step 3: Click on the extension and then Register to create a new account or Sign-In if the account is already created
- Step 4: Click on Show/Hide Test network on the top-left corner of the Metamask window and select Ropsten Test Network
- Step 5: Copy the Metamask wallet address and then use it to get test Ethers from Ropsten testnet faucets
 

Remix IDE
- Step 1: Navigate to https://remix.ethereum.org/ 
- Step 2: The user can either use the default workspace or connect to the localhost to use the project repository stored on the local machine
- Step 3: Create the smart contract file with the extension (*.sol). The file DeployedContract.sol has been created for this project.
- Step 4: Write the required code in the contract file which includes the name and symbol for the ERC-20 token
		Name: 21151334_Prawal
		Token: PSB
- Step 5: Since we have used solidity version 0.8.0 in the code, then we have to compile the contract file using the same version. Click on Compile on the left hand tab of Remix.
- Step 6: Once the contract file is compiled, go to the third tab on the left to deploy the contract through Metamask. The remix tool will automatically pickup the Metamask wallet address through the Metamask plugin installed earlier. Else, the user can do it manually by copying the Metamask wallet address and pasting it in Remix under account on Deploy Tab. 
- Step 7: The user then has to select the Injected Web3 as environment and ERC20 under contract dropdown. Once done, then click on Deploy at the bottom of the tab.
- Step 8: Navigate to Metamask plugin on the top-right corner of Chrome menu to check the status of Contract Deployment
- Step 9: The user can then click on “View on Block Explorer” to check the contract status and details on Etherscan.


Infura
- Step 1: Navigate to www.infura.io. Register to create a new account or sign-in if the account already exists.
- Step 2: Create the first project by entering the Product as Ethereum and project name as NCI
- Step 3: Select the project NCI and navigate to project settings
- Step 4: Select the endpoint as Ropsten and copy the project ID. This project ID will be used in (.env) file for the project configuration.


Node.js
- Step 1: Download Node.js package installer for your respective OS from https://nodejs.org/en/download/
- Step 2: Run the installer
- Step 3: Once installed, open Terminal or command prompt and install the following dependencies

-		npm install big-number
-		npm install dotenv
-		npm install ethereumjs-tx
-		npm install web3


Executing the Application Code
Use an editor such as Sublime Text to write application code
- Step 1: Create file accounts.txt and write the receiver's wallet addresses
- Step 2: Create file (*.env)
- Step 3: Create file contract.js and write the required code
- Step 4: Create file distribute.js and write the required code
- Step 5: Open Terminal / Command Prompt
- Step 6: Change the directory to the folder where the application code files are stored
- Step 7: Execute the file distribute.js using the following command
- 
		node distribute.js
                
- Step 8: This might take a few minutes to execute
- Step 9: Once executed successfully, navigate to the contract details on Etherscan and check the details. As per the application code written for our project, equal number of tokens PSB (~5000) each will have been transferred successfully to the 10 Wallet Addresses mentioned in the file accounts.txt


DockerHub
- Step 1: Open www.docker.io and create your account
- Step 2: Download docker desktop for your OS and install it on your machine
- Step 3: Open Terminal / command prompt and navigate to your project folder
- Step 4: Run Command docker to verify docker installation
- Step 5: Run Command vi Dockerfile to create Dockerfile which will be used to create image and then the container
- Step 6: Run command 
-       docker build . -t node-blockchain-new
- Step 7: Run the command 
-       docker run -it <image-id>
- Step 8: Login to docker in the browser and create a public repository. Copy the repository name to be used in further steps
- Step 9: Run the command 
-       docker tag node-blockchain-new:latest prawalsaxena/blockchain:node-blockchain-new
- Step 10: Run the command 
-       docker push prawalsaxena/blockchain:node-blockchain-new
- Step 11: Go to docker in the browser, navigate to the container and then to the Tab container to get the pull command for the respective container 
-       docker pull prawalsaxena/blockchain:node-blockchain-new
-       docker run prawalsaxena/blockchain:node-blockchain-new 

Github
- Step 1: Login to Github and create an account / sign-in
- Step 2: Create a public repository (Blockchain)
- Step 3: Navigate to project code folder through Terminal
- Step 4: Execute the following commands
        
-		git init
-		git add README.md
-		git commit -m "Blockchain-files"
-		git branch -M main
-		git remote add origin https://github.com/x21151334-Prawal/Blockchain.git
-		git push -u origin main
-       git colne https://github.com/x21151334-Prawal/Blockchain.git
       
