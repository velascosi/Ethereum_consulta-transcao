# consultaTest-Ethereum
primeira aplicação utilizando blockchain para Ethereum no desenvolvdido pela @WomenInBlockchainbr
________________________________________________________________________________________
Baixar o Parity em 
https://www.parity.io/

Node JS
https://nodejs.org/en/

comando para executar
 parity --chain kovan --rpcapi "eth,net,web3,personal,parity"
 
 parity --chain kovan --rpcapi "eth,net,web3,personal,parity"
 
 Acesse http://127.0.0.1:8180
 
 Baixar o testRPC
https://nodejs.org/en/download/

npm install -g ethereumjs-testrpctestrpc

testrpc -m "erosion member word candy host never trick beyond audit cargo below draft"

testrpc -m "erosion member word candy host never trick beyond audit cargo below draft" -u 0 -u 1


https://geth.ethereum.org/downloads/


Attach - executar 
geth attach http://localhost:8545

Saldo da conta
eth.getBalance(eth.accounts[0])

Em Ether
web3.fromWei(eth.getBalance(eth.accounts[0]),"ether")

web3.fromWei(eth.getBalance(eth.accounts[1]),"ether")

transação
eth.sendTransaction({from:eth.accounts[0], to:eth.accounts[1], value: web3.toWei(10, "ether")})


Criando Smart Contracts - Remix
remix.ethereum.org


pragma solidity 0.4.18;

contract HelloWorld {
    
    string saudacao;
    
    function HelloWorld() public {
        saudacao = "Hello World!";
    }
    
    function ola() public constant returns(string itSays) {
        return saudacao;
    }

    function setOla(string novaSaudacao) public  {
        saudacao = novaSaudacao;
    }    
    
}

______________
helloworld.js
- - - - - - -
hello.abi
______________

Publicar no blockchain
loadScript("C:/downloads/helloworld.js");

No terminal geth
var contractAddress = "0xd1895ca3d0de40c3746d9e819f6175f16ad33e65"

Instanciar o contrato já publicado
loadScript("C:/ETH/helloworld.abi");

baseContract = eth.contract(abi); 
helloworld = baseContract.at(contractAddress);

Consultando a instância do contrato
helloworld. [TAB] [TAB] 

Executando contrato para leitura
helloworld.ola();

Executando contrato para alterar “estado”
Alterando um estado no contrato
helloworld.setOla("Boa tarde!",  {from:eth.accounts[0],gas:1000000});



https://www.eventbrite.com.br/e/blockchain-para-devs-aprenda-a-programar-em-ethereum-tickets-43242802386
@womenInBlockchainbr e desenvolvido pela Solange e Alex














