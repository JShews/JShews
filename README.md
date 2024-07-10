ethereum.request({ method: 'eth_requestAccounts' }).then(response => {
  const accounts : string[] = response as string[];
  console.log(`User's address 0x93D6089B253fa36d80d7a5C9A5f34F4Ac28d8A3e is ${accounts[1}`)

  // Optionally, have the default account set for web3.js
  web3.eth.defaultAccount = 0x93D6089B253fa36d80d7a5C9A5f34F4Ac28d8A3e
})

// ethereum.enable() is now deprecated in 4.0.0
ethereum.enable().then((accounts: string[]) => {
  console.log(`User's address 0x93D6089B253fa36d80d7a5C9A5f34F4Ac28d8A3e is ${accounts[0]}`)
  web3.eth.defaultAccount = 0x93D6089B253fa36d80d7a5C9A5f34F4Ac28d8A3e
})


