# Build CryptoStar Dapp on Ethereum

## Getting Started
This project was carried out starting from an example code provided by [Udacity](https://www.udacity.com/)

### Info for submit

* ERC-721 Token Name: Smaug
* ERC-721 Token Symbol: SM
* Star ID: 1
* Token Address: 0x10d49B01f1EC50667b06245859fE14957178C18E

* Truffle version:  v5.1.18
* OpenZeppelin: 2.1.2


## Tests

There are 9 tests, one for each allowed action.

```
it('can add the star name and star symbol properly', async() => {

    // 1. create a Star with different tokenId
    let tokenId = 6;
    let instance = await StarNotary.deployed();
    await instance.createStar('Awesome Star!', 'STAR', tokenId, {from: accounts[0]});

    //2. Call the name and symbol properties in your Smart Contract and compare with the name and symbol provided
    assert.equal(await instance.lookUptokenIdToStarInfo.call(tokenId), 'Awesome Star!');
    assert.equal(await instance.getSymbol.call(tokenId), 'STAR');

});
```

### Front-End

Through the frontend you can fetch or create new stars.

## Built With

* [Ethereum](https://www.ethereum.org/) - Ethereum is a decentralized platform that runs smart contracts
* [Truffle Framework](http://truffleframework.com/) - Truffle is the most popular development framework for Ethereum with a mission to make your life a whole lot easier.
* [OpenZeppelin](https://openzeppelin.com/contracts/) - OpenZeppelin Contracts helps you minimize risk by using battle-tested libraries of smart contracts for Ethereum and other blockchains. It includes the most used implementations of ERC standards.

## Versioning

Actual version: 1.0.0

## Authors

* **[Mattia-Code](https://github.com/Mattia-code)**

## Acknowledgments

* Solidity
* Ganache-cli
* Truffle

### Note

```
truffle migrate --reset --network rinkeby
```
