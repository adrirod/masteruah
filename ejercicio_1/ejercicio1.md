# Ejercicio 1

Primero se debe crear el fichero genesis.json. Para ello se utiliza el comando:
```console
cat > genesis.json
```

Pasamos a rellenar el fichero con la información necesaria para iniciar la cadena de loques.

Posteriormente, pasamos a inicializar el cliente Geth:
```console
geth init genesis.json --datadir block_data
```

Antes de comenzar a minar hay que crear la cuenta etherbase y una personal, para ello hay que abrir la consola de geth:
```console
geth --networkid 123 --datadir data_block console 
```

Inicializada, se pasa a crear una nueva cuenta, la primera que se cree será la coinbase:
```console
personal.newAccount()
```
0xae348a3982157e49174d5fdb4fcd1235acef0037

La segunda será la personal:

"0xe0613172db97c1708401dca784d9e3e0e1c6191f"

Creadas ambas, se comienza a minar:
```console
miner.start()
```
Tras minar unos bloques, paramos el minado con:
```console
miner.stop()
```

Podemos comprobar el balance de las dos cuentas de la siguiente forma:
```console
eth.getBalance("0xae348a3982157e49174d5fdb4fcd1235acef0037")
```
Devuelve: 645000000000000000000
```console
eth.getBalance("0xe0613172db97c1708401dca784d9e3e0e1c6191f")
```
Devuelve: 0
