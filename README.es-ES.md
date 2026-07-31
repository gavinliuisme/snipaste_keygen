## Descripción

Este proyecto analiza y resume la activación offline de Snipaste v2.11.3 para Windows.

Este proyecto hace referencia al artículo: [Snipaste-2.10.8-x64 离线激活记录 - DirWangK - 博客园](https://www.cnblogs.com/DirWang/p/19258416).

## Pasos Detallados

### Caso 1: Activación en la máquina local

#### Instalar librerías de Python de terceros

`pip install -r requirements.txt`

#### Reemplazar el binario parcheado (patched)

Reemplazar `Snipaste.exe` en el directorio del programa Snipaste por `Snipaste_patched.exe`.

#### Generar número de serie

`python keygen\main.py ` 

Ejemplo de salida:

```
--------------------------------------------------
The activation code for the host machine is:
0w-vKrYmZZXP0Tv0xxxxxxx1FPZccEzL4dao8L7xt6HtDbWOBJfbeGm7U7SHvvUxEpWz6U2TptvaiI88G8yrwAYBaMh0JmWVz9E7dgjZ+RGhuRfXy6xxxxxxxxxkt/mXP28RBIBjS6Y1SD86AATr5dqIxbSm9S0HqNIDl8UDFvVwu1exY7k1nWvR2BoDDRQv4CZ4JOhOTFyCrhSqvJCKQN3SfxxxxxxxxxxG7L3q7x0raWDbrUCx+sJ1lynR6unisNNm0/+DUFbUKu2x72kJ18U91jqmC8APnqs2VhQS9dAA6NrMfKJ2ESJ+pyrNMQbeK0N8Xjmm5MzKIRf10DilnPOrgI++OlVj9E
--------------------------------------------------
```

### Caso 2: Activación de cliente remoto

#### Operaciones del cliente

##### Reemplazar el binario parcheado (patched)

Reemplazar `Snipaste.exe` en el directorio del programa Snipaste por `Snipaste_patched.exe`.

##### Obtener información del dispositivo cliente

Ejecutar `client.exe`. Puede descargarse desde https://github.com/1226357697/snipaste_keygen/releases/download/v1.0/client.exe.

Ejemplo de salida:

````
The device information is H4sIAAAAAAAA/wE0AMv/eyJkxxxxxxxxxx5TRSIsIm1hY2hpbmVpZCI6IkRFRkItOTExM0Y1OTYtOURENjdxxxxxxxxxxRA0AAAA
````

#### Lado del generador (keygen)

##### Instalar librerías de Python de terceros

`pip install -r requirements.txt`

##### Generar número de serie

`python keygen\main.py -n [name] -d [device_info]`

Ejemplo: `python keygen\main.py -n ikun -d H4sIAAAAAAAA/wE0AMv/eyJkxxxxxxxxxx5TRSIsIm1hY2hpbmVpZCI6IkRFRkItOTExM0Y1OTYtOURENjdxxxxxxxxxxRA0AAAA`

Ejemplo de salida:

```
--------------------------------------------------
The activation code for the client machine is:
0w-vKrYmZZXP0Tv0xxxxxxx1FPZccEzL4dao8L7xt6HtDbWOBJfbeGm7U7SHvvUxEpWz6U2TptvaiI88G8yrwAYBaMh0JmWVz9E7dgjZ+RGhuRfXy6xxxxxxxxxkt/mXP28RBIBjS6Y1SD86AATr5dqIxbSm9S0HqNIDl8UDFvVwu1exY7k1nWvR2BoDDRQv4CZ4JOhOTFyCrhSqvJCKQN3SfxxxxxxxxxxG7L3q7x0raWDbrUCx+sJ1lynR6unisNNm0/+DUFbUKu2x72kJ18U91jqmC8APnqs2VhQS9dAA6NrMfKJ2ESJ+pyrNMQbeK0N8Xjmm5MzKIRf10DilnPOrgI++OlVj9E
--------------------------------------------------
```

## TODO

- [ ] Automatizar el parcheo de `Snipaste.exe` en el directorio del programa mediante `client.exe`.

## Capturas de pantalla

![效果图](./assets/效果图.png)

## Imagen del parche
Solo se parcheó un valor de retorno.
![效果图](./assets/补丁图.png)
