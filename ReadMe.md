<h2>Felt Value Converter Tool - Deployment</h2><h3>Prerequisites</h3><p>Before proceeding with the deployment using the ArgentX Wallet, make sure you have completed the following steps:</p><ol><li><p>Install Python 3.x on your system.</p></li><li><p>Install the required Python packages by running:</p><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><button class="flex ml-auto gap-2"><svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" class="h-4 w-4" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path><rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect></svg>Copy code</button></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs">pip install openzeppelin-cairo-contracts
</code></div></div></pre></li><li><p>Set up the StarkNet environment by following the instructions in the <a href="https://docs.starknet.io/documentation/getting_started/environment_setup/" target="_new">StarkNet documentation</a>.</p></li><li><p>Install Nile, a StarkNet testnet, by following the setup instructions in the <a href="https://github.com/OpenZeppelin/nile" target="_new">Nile repository</a>.</p></li><li><p>Compile the smart contract with the Felt values by running the following command inside your smart contract project directory:</p><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><span>python</span><button class="flex ml-auto gap-2"><svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" class="h-4 w-4" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path><rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect></svg>Copy code</button></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs language-python">nile <span class="hljs-built_in">compile</span>
</code></div></div></pre></li><li><p>Make sure you have the ArgentX Wallet application installed and set up.</p></li></ol><h3>Deployment Steps</h3><ol><li><p>Run the Felt Value Converter Tool</p><p>First, run the Felt Value Converter tool (<code>felt_converter.py</code>) to generate the required data for deployment. Modify the variables (<code>name</code>, <code>symbol</code>, <code>tokenUri</code>, <code>token_uri_suffix</code>) with your desired values.</p><pre><div class="bg-black rounded-md mb-4"><div class="flex items-center relative text-gray-200 bg-gray-800 px-4 py-2 text-xs font-sans justify-between rounded-t-md"><button class="flex ml-auto gap-2"><svg stroke="currentColor" fill="none" stroke-width="2" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round" class="h-4 w-4" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path><rect x="8" y="2" width="8" height="4" rx="1" ry="1"></rect></svg>Copy code</button></div><div class="p-4 overflow-y-auto"><code class="!whitespace-pre hljs">python felt_converter.py
</code></div></div></pre><p>This will generate the <code>output.txt</code> file, which will contain the necessary information for the constructor.</p></li><li><p>Retrieve Constructor Parameters</p><p>Open the <code>output.txt</code> file and copy the following constructor parameters:</p><ul><li><code>Name</code>: The token name in plain text.</li><li><code>Symbol</code>: The token symbol in plain text.</li><li><code>Token URI Suffix</code>: The token URI suffix in plain text.</li><li><code>Token URIs</code>: The list of token URIs with their corresponding Felt values.</li></ul><p>Make sure to keep these parameters handy for the deployment process.</p></li><li><p>Deploy the Smart Contract with ArgentX Wallet</p><p>Follow these steps to deploy the compiled smart contract using the ArgentX Wallet:</p><ul><li><p>Open the ArgentX Wallet application.</p></li><li><p>Navigate to the StarkNet dApp deployment page.</p></li><li><p>Provide the required constructor parameters based on the information from the <code>output.txt</code> file.</p></li><li><p>Deploy the compiled smart contract to the StarkNet testnet (Nile).</p></li><li><p>Confirm the deployment transaction using the ArgentX Wallet.</p></li><li><p>Wait for the deployment to be confirmed on the StarkNet testnet.</p></li></ul></li><li><p>Test and Interact with the Deployed Smart Contract</p><p>After successfully deploying the smart contract, you can test and interact with it using the ArgentX Wallet or other StarkNet-compatible wallets. Ensure that you use the correct contract address and ABI to interact with the deployed contract.</p></li></ol><p>Congratulations! You have successfully deployed a smart contract on the StarkNet testnet (Nile) using the ArgentX Wallet. You can now explore the capabilities of your deployed contract and its interactions on the StarkNet testnet.</p>