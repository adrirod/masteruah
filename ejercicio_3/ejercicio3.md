# Ejercicio 3

Primero nos conectamos a la red Rinkeby, para ello usamos el comando:
```console
geth --rinkeby
```
Para obtener el bloque genesis:
```console
admin.nodeInfo
```
```console
{
  enode: "enode://61dab53c48695c62c46433724d71fa3c966d0b56932427a77a1e08752c985d89b125b8ca2161305041fe8ddfd9cd2de0639589d32582fa207704bd5a6fa78445@127.0.0.1:30304",
  enr: "0xf896b840da2c34e09c6f9602f35b9f5665052bd50a4d9655103653e3fb0a98445840e4b9147cfa9901d71190bdfe0f38592bf77bd89d88e83ecc46ce5a4d57d1ef2dc4f70883636170c6c5836574683f826964827634826970847f00000189736563703235366b31a10361dab53c48695c62c46433724d71fa3c966d0b56932427a77a1e08752c985d898374637082766083756470827660",
  id: "79e31826a5afbe6f0531b2cec224ebd114207133235743d4652c89a1a4f95819",
  ip: "127.0.0.1",
  listenAddr: "[::]:30304",
  name: "Geth/v1.8.27-stable-4bcc0a37/linux-amd64/go1.10.4",
  ports: {
    discovery: 30304,
    listener: 30304
  },
  protocols: {
    eth: {
      config: {
        byzantiumBlock: 4370000,
        chainId: 1,
        constantinopleBlock: 7280000,
        daoForkBlock: 1920000,
        daoForkSupport: true,
        eip150Block: 2463000,
        eip150Hash: "0x2086799aeebeae135c246c65021c82b4e15a2c451340993aacfd2751886514f0",
        eip155Block: 2675000,
        eip158Block: 2675000,
        ethash: {},
        homesteadBlock: 1150000,
        petersburgBlock: 7280000
      },
      difficulty: 17179869184,
      **genesis: "0xd4e56740f876aef8c010b86a40d5f56745a118d0906a34e69aec8c0db1cb8fa3",**
      head: "0xd4e56740f876aef8c010b86a40d5f56745a118d0906a34e69aec8c0db1cb8fa3",
      network: 1
    }
  }
}
```


Para obtener los peers a los que estoy conectado he utilizado el siguiente comando:
```console
web3.net.peerCount
```

Para obtener información sobre ellos he utilizado:

admin.peers
```javascript
Lo cual ha devuelto:

[{
    caps: ["eth/62", "eth/63"],
    enode: "enode://343149e4feefa15d882d9fe4ac7d88f885bd05ebb735e547f12e12080a9fa07c8014ca6fd7f373123488102fe5e34111f8509cf0b7de3f5b44339c9f25e87cb8@52.3.158.184:30303",
    id: "1aabba770181eef1b399df4e4177cfc797a1ef5efb0bf961f455c6cab30bee5f",
    name: "Geth/v1.9.0-unstable-2da6d1e0-20190613/linux-amd64/go1.12",
    network: {
      inbound: false,
      localAddress: "192.168.1.39:51290",
      remoteAddress: "52.3.158.184:30303",
      static: false,
      trusted: false
    },
    protocols: {
      eth: {
        difficulty: 8349139,
        head: "0x2693f50368c97447f385cf61b883f7c411fbf7dda5be9ef3d46af347c9cae284",
        version: 63
      }
    }
}, {
    caps: ["eth/62", "eth/63", "les/2"],
    enode: "enode://b6b28890b006743680c52e64e0d16db57f28124885595fa03a562be1d2bf0f3a1da297d56b13da25fb992888fd556d4c1a27b1f39d531bde7de1921c90061cc6@159.89.28.211:30303",
    id: "56483dbe3073c57241c3f128a6ca1c4018347cc0afd0ea1db6773c7e2794698b",
    name: "Geth/v1.9.0-unstable-97d36156-20190517/linux-amd64/go1.12.5",
    network: {
      inbound: false,
      localAddress: "192.168.1.39:38252",
      remoteAddress: "159.89.28.211:30303",
      static: false,
      trusted: false
    },
    protocols: {
      eth: {
        difficulty: 8156838,
        head: "0x4efb29b6cbdebd02e9d8cc642f59ba88e4a4503730702e7a26e41014ab4159c9",
        version: 63
      }
    }
}, {
    caps: ["eth/62", "eth/63", "les/2", "les/3"],
    enode: "enode://59f9c651a31269aa802e5f62c5ec91b6de5faf7b8ef4d96382febe896b830284682659aae158d3650ff99b198f889f7c7c032b885c4551ea2d2d6c772343e962@52.236.164.12:30303",
    id: "c65b921f9a2230edec169bd18f2eb8b040b7a9ab95421d1ac4e0a969fa3eee77",
    name: "Geth/v1.9.0-unstable-79c90dce-20190613/linux-amd64/go1.10.4",
    network: {
      inbound: false,
      localAddress: "192.168.1.39:38216",
      remoteAddress: "52.236.164.12:30303",
      static: false,
      trusted: false
    },
    protocols: {
      eth: {
        difficulty: 8349119,
        head: "0xd3737b661cfdf5bca89f97cee4765be4ddf1f47c98d14b916fea72cee802cfeb",
        version: 63
      }
    }
}, {
    caps: ["eth/62", "eth/63"],
    enode: "enode://3d5659c962081fc3a9b17d28a9cceaa06bfa2233e07db0df27fff235a126200af59a86768c139c61e6285e8c901ad9f598e14dad24cff49f31c89f16c7e6ceb7@69.127.0.122:30303",
    id: "e3d83346cf1286f83429c4e62809ae4ef40ddd16610ecf77803ab20917f3221f",
    name: "Geth/v1.8.27-stable/darwin-amd64/go1.12.5",
    network: {
      inbound: false,
      localAddress: "192.168.1.39:45886",
      remoteAddress: "69.127.0.122:30303",
      static: false,
      trusted: false
    },
    protocols: {
      eth: {
        difficulty: 8349145,
        head: "0xc878b3e83ae86956ff96ec68cbfa747d43f400a142966d8f990bb09ba6a4b5c9",
        version: 63
      }
    }
}]
```
Por último para añadir manualmente un bootnode:
```console
bootnode --genkey=boot.key
bootnode --nodekey=boot.key
```
Siendo la respuesta:
```console
INFO [06-15|19:23:24.310] New local node record                    seq=1 id=45c0696cac56563c ip=<nil> udp=0 tcp=0
```

