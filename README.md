# dds-plantuml-ejemplo
Ejemplo de uso de la herramienta 
[plantUML](https://plantuml.com/es/class-diagram) en un readme de GitHub

![ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/dds-plantuml-ejemplo/main/ejemplo.puml)

## Pasos a seguir
### Paso 1

Obtener la URL hacia el raw del archivo PlantUML, la cual tiene el formato:
```
https://raw.githubusercontent.com/{OWNER}/{REPO}/{BRANCH}/{COMMIT}?/{RUTA_ARCHIVO}.puml
```
_El commit es opcional. Si no se incluye, se toma por defecto el último
commit en la branch._

Por ejemplo:
```
https://raw.githubusercontent.com/RaniAgus/dds-plantuml-ejemplo/main/ejemplo.puml
```
#### Nota sobre repositorios privados

Si el archivo plantuml se encuentra en un repo privado, para acceder al raw se 
necesita de un token que se agrega al final del link en forma de query param, 
por lo que el link quedaría así:
```
https://raw.githubusercontent.com/{OWNER}/{REPO}/{BRANCH}/{COMMIT}?/{RUTA_ARCHIVO}.puml?token={TOKEN}
```
Estos tokens se generan por cada commit, por lo que para que nuestra solución
perdure hay que cambiar el campo `BRANCH` por el hash del commit 
correspondiente y agregar el `TOKEN` (y acordarse de irlos actualizando).

La opción más sencilla es, desde GitHub, ir al archivo en el commit correcto y
de ahí copiar el link al raw del archivo. Podés encontrar al final del readme 
una [mini guía de cómo hacerlo](#cómo-acceder-al-raw-de-un-archivo).

### Paso 2

Vamos a usar el servicio de [Proxy](https://plantuml.com/server) de PlantUML
para conseguir el link que vamos a insertar en nuestro README.md
```
http://www.plantuml.com/plantuml/proxy?cache=no&src={LINK_RAW}
```
Por ejemplo:
```
http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/dds-plantuml-ejemplo/main/ejemplo.puml
```
### Paso 3

Pegar esa URL como imagen en el README.md, en formato Markdown:
```
![texto alternativo]({LINK_PLANTUML})
```

Por ejemplo:
```
![ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/dds-plantuml-ejemplo/main/ejemplo.puml)
```
El resultado es el que está 
[al principio de este readme](#dds-plantuml-ejemplo).

## Cómo acceder al raw de un archivo

1. Ir a la sección "commits" del repo:

![image](https://user-images.githubusercontent.com/39303639/119248270-6b870080-bb66-11eb-8787-98c5e91818d1.png)

2. Buscar el commit y hacer en `<>` para ver el estado del repo en ese commit:

![image](https://user-images.githubusercontent.com/39303639/119248857-54e2a880-bb6a-11eb-84fe-cbd8631bc1e0.png)

3. Moverse hacia el archivo en cuestión y hacer click en `View raw`:

![image](https://user-images.githubusercontent.com/39303639/119248910-cfabc380-bb6a-11eb-95de-d1c5bd3c3054.png)

Esto nos va a llevar al mismo link que vamos a necesitar para el 
[paso 1](#paso-1).

## Créditos

Este método fue extraído del siguiente comentario en StackOverflow: https://stackoverflow.com/a/32771815/14089741
