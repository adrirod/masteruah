# Ejercicio 2

##Con Geth

Pasamos a transferir de la cuenta 0xae348a3982157e49174d5fdb4fcd1235acef0037 a
0xe0613172db97c1708401dca784d9e3e0e1c6191f unos ethers. Para ello usamos debemos desbloquear la primera cuenta con el comando:

```console
personal.unlockAccount(eth.accounts[0], "password")
```

```console
eth.sendTransaction({from:eth.accounts[0], to:eth.accounts[1], value: web3.toWei(1, "ether")})
```
Si todo ha ido correctamente saldra un mensaje como el de la imagen geth_transaction.png.

Ahora hay que minar para que los fondos aparezcan en la cuenta destino, para ello usamos
```console
miner.start()
```
Dejamos minar unos bloques y lo paramos con miner.stop().

Pasamos a comprobar los balances:
```console
eth.getBalance(eth.accounts[0])
```
**809000000000000000000**
```console
eth.getBalance(eth.accounts[1])
```
**1000000000000000000**

(Ver imagen geth_result.png)

##Con Ganache y Truffle

Primero, hay que comprobar las cuentas disponibles:
```console
web3.eth.getAccounts()
```
Seleccionamos las dos primeras:

0x03D804075fFE9dC6b14a4CA0bA7E550E926cF9Aa

0xfca9A17236890214c242450a5b3e3F7DeBF1A0Db

Pasamos a comprobar los balances de las mismas:
```console
web3.eth.getBalance("0x03D804075fFE9dC6b14a4CA0bA7E550E926cF9Aa")

web3.eth.getBalance("0xfca9A17236890214c242450a5b3e3F7DeBF1A0Db")
```
(ver imagen truffle_prev.png)

Para mayor claridad creamos una variable donde guardaremos la cantidad a traspasar:
```console
 var amount = web3.utils.toWei('1', 'ether')
```
Y realizamos la transferencia:
```console
web3.eth.sendTransaction({from:"0x03D804075fFE9dC6b14a4CA0bA7E550E926cF9Aa", to:"0xfca9A17236890214c242450a5b3e3F7DeBF1A0Db", value: amount})
```
(ver imagen truffle_transac.png)

Comprobamos si efectivamente se ha realizado, ver imagen truffle_result.png
