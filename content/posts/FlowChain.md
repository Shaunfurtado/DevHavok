+++
title = "FlowChain"
linktitle = "FlowChain"
date = 2023-12-03T18:08:23+05:30
draft = false
tags = ['Projects' ]
+++
## WEb3 based supply chain management system
![img](https://i.imgur.com/mpXFh6z.png)
![img](https://i.imgur.com/LgqEL84.png)
![img](https://i.imgur.com/3KF2mit.png)
![img](https://i.imgur.com/4uZcInx.png)
![img](https://i.imgur.com/Doh5W7n.png)

### Used packages:-
- hardhat@2.19.2
- ethers@5.7.2
- web3modal@1.9.12
- react@18
- react-qr-code
- react-qr-scanner

### To run this app
```
npm install
```
```
npx hardhat init
```
```
npx hardhat node
```
```
npx hardhat run --network localhost scripts/deploy.js 
```
Now, move the Tracking.Json file which is created in ./artifacts/contracts/ to ./src/components/Context/
to accesss the Tracking ABI of the smart contracts.

### Run the React app with development server
```
npm run start
```

Now, go to [localhost:3000](localhost:3000)
