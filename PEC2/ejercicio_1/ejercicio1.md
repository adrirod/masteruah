# Ejercicio 1

Se ha utilizado el fichero **ensutils-testnet.js**. Al cual se ha introducido una modificacion para que apunte a la red rinkeby.

Tras ello, nos sincronizamos en modo light a la red rinkeby:

```console
geth -rinkeby -syncmode "fast"
```

Tras sincronizarnos al 100% podemos realizar el ejercicio:
Cargamos el javascript comentado anteriormente:

```console
loadScript("/home/adri/Proyectos/CryptoZombies/ensutils-testnet.js")
```
Comprobamos si está libre el dominio:

```console
testRegistrar.expiryTimes(web3.sha3("arpEther"))
```
Lo cual nos devuelve 0 (ver imagen comprobacion_ens.png), entonces quiere decir que está libre.

Pasamos a desbloquear la cuenta (ver imagen desbloqueo_account.png)
```console
personal.unlockAccount(eth.accounts[0])
```

Tras desbloquear la cuenta pasamos a registra el dominio: (ver imagen registro_dominio.png)
```console
testRegistrar.register(web3.sha3("arpEther"), eth.accounts[0], {from: eth.accounts[0]})
```

Volvemos a comprobar si el dominio está utilizado (ver imagen registro_dominio.png)
Por último, comprobación del owner del dominio:

```console
ens.owner(namehash("arpEther.test"))
```
(Ver imagen owner_dominio.png)
