ethereum.request({ method: 'eth_requestAccounts' }).then(response => {
  const accounts : string[] = response as string[];
  console.log(`User's address is ${accounts[0]}`)

  // Optionally, have the default account set for web3.js
  web3.eth.defaultAccount = accounts[0]
})

// ethereum.enable() is now deprecated in 4.0.0
ethereum.enable().then((accounts: string[]) => {
  console.log(`User's address is ${accounts[0]}`)
  web3.eth.defaultAccount = accounts[0]
})


