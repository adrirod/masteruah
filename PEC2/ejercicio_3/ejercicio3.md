# Ejercicio 3

Primero, se crea el fichero html (se encuentra en esta carpeta) junto con los documentos con los que se enlaza. 

Segundo, se intenta subir los documentos con el siguiente comando:
```console
swarm --recursive --defaultpath swarm-manifest/index.html --bzzapi http://swarm-gateways.net/ up swarm-manifest/ 2> up.log
```
Sin embargo, da el siguiente error:
```console
Fatal: Upload failed: unexpected HTTP status: 308 Permanent Redirect
```
Por ello, se pasa a subirlo con el comando modificado:
```console
swarm --recursive --defaultpath swarm-manifest/index.html up swarm-manifest/ 2> up.log
```
Consiguiendo subirlo todo dando el hash:
**7928780620d70c668ff4ce117bb22763a65bac67721892d34a352ec9924cbc3f**
(ver imagen swarm_manifest.png)

Cuando se prueba con la url :
https://swarm-gateways.net/bzz:/7928780620d70c668ff4ce117bb22763a65bac67721892d34a352ec9924cbc3f/
No funciona.

Sin embargo cuando se prueba con: http://localhost:8500/bzz:/7928780620d70c668ff4ce117bb22763a65bac67721892d34a352ec9924cbc3f/
Funciona corretamente.
 La url del documento 1:
 chrome-extension://oemmndcbldboiebfnladdacbdfmadadm/http://localhost:8500/bzz:/7928780620d70c668ff4ce117bb22763a65bac67721892d34a352ec9924cbc3f/bloque3.pdf
 La url del documento 2:
 http://localhost:8500/bzz:/7928780620d70c668ff4ce117bb22763a65bac67721892d34a352ec9924cbc3f/cat.jpg
 
 Se adjuntan capturas de las urls.


