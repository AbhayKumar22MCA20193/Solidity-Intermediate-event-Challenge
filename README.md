# Solidity-Intermediate-event-Challenge
Sample Project Instructions
After cloning the github, you will want to do the following to get the code running on your computer:

Inside the project directory, in the terminal type: npm i
Open two additional terminals in your VS code
In the second terminal type: npx hardhat node
In the third terminal, type: npx hardhat run --network localhost scripts/deploy.js
Back in the first terminal, type: npx hardhat console --network localhost
Then we'll use this command to attach our smart contract to our console: const bank = await (await ethers.getContractFactory("Bank")).attach("0x5FbDB2315678afecb367f032d93F642f64180aa3")
Once the contract is attached, you can go ahead and call the smart contract functions!
Here is an example you can run using our hardhat provided accounts:

await bank.deposit("0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266", 1)
await bank.getBalance("0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266")
await bank.transfer("0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266", "0x70997970C51812dc3A010C7d01b50e0d17dc79C8", 1)
await bank.getBalance("0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266")
await bank.getBalance("0x70997970C51812dc3A010C7d01b50e0d17dc79C8")
await bank.withdraw("0x70997970C51812dc3A010C7d01b50e0d17dc79C8", 1)
await bank.getBalance("0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266")
Event Challenge
Let's practice what we've learned about events. To do this:

Write a smart contract that defines and triggers 3-4 events
Index the events so that they can be easily searched
Capture these events in your JavaScript code
