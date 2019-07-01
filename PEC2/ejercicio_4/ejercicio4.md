# Ejercicio 4

Proyecto utilizado está desplegado en Ganache

Se inicializa la conexión con Swarm:
```console
swarm --bzzaccount 5be5cb0dea26d2c5a6b9e5c562eadb0b534b802a
```
Se suben los ficheros:
```console
swarm --recursive up ./src
```
Se comprueba que se pueda acceder a los ficheros, ver imagenes.

Se vuelve a inicializar swarm, pero esta vez con la API de ENS:
```console
 swarm --ens-api $HOME/.ethereum/rinkeby/geth.ipc --bzzaccount 5be5cb0dea26d2c5a6b9e5c562eadb0b534b802a
 ```
 
 Se procede a relacionar el dominio con el contenido:
 ```console
publicResolver.setContent(namehash('arpEther.tst'),'0x5b5ffbca02b04347298f11628ba145469c0c5e8c2ea44366583b9cd5d1da4355', {from: eth.accounts[0], gas: 100000})
```
Ver captura set_resolver.png.


