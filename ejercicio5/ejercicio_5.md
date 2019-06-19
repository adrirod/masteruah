# Ejercicio 5
Para la obtención de los identificadores he utilizado la siguiente web: 

https://emn178.github.io/online-tools/keccak_256.html

La utilización de la misma es para obtener el hash completo del literal nombre de funcion y parámetros, por ejemplo,
sumValues(uint,uint)

Una vez obtenido se corta el hash para quedarnos solo con los primeros 4 bytes

-function sumValues (uint _a, uint _b) public view returns (uint _c) {}
(ver imagen hash_sumvalues.png) 
**Identificador: 0x06cbb87**

-function getGasDetails() public payable{}
(ver imagen getDetails_hash.png) 
**Identificador:*0x3d86f4a*

-function __callback(bytes32 id, string memory result) public{}
(ver imagen callback_hash.png) 
**Identificador:0x27dc297**

-function arp(uint8 _a, address _address) internal{}
(ver imagen arp_hash.png) 
**Identificador:*0x4d766f3*
