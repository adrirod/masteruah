# Ejercicio 2

**Las imagenes se encuentran en la carpeta de imagenes**

Se va a utilizar el proyecto pet-shop-tutorial. **Este proyecto está desplegado en una red local con Ganache**

Se inicializa IPFS:

```console
ipfs daemon
```
(ver imagen ipfs_daemon.png)

La subida de los ficheros se realiza con el comando:
```console
ipfs add -r src/
```

Se adjunta captura donde se muestra la finalización de la carga. ver imagen  ipfs_cargado.png.

Copio el hash de la carpeta:

```console
added QmSXkvV51kaLzV3WEEHDnZpNqQzgWV5S6xsLvRoiAQ6P3N src/
```
http://127.0.0.1:8080/ipfs/QmSXkvV51kaLzV3WEEHDnZpNqQzgWV5S6xsLvRoiAQ6P3N/

Por último, se configura un pin:

```console
ipfs pin add -r QmSXkvV51kaLzV3WEEHDnZpNqQzgWV5S6xsLvRoiAQ6P3N
```
ver imagen ipf_pin.png
