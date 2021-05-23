# dds-plantuml-ejemplo
Ejemplo de uso de la herramienta 
[plantUML](https://plantuml.com/es/class-diagram) en un readme de GitHub

![ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/d164f69b39ea5a5b125bf1cee13acd15718cd5a9/ejemplo.puml)

## Pasos a seguir
### Paso 1

Obtener la URL hacia el raw del archivo PlantUML, la cual tiene el formato:
```
https://raw.githubusercontent.com/{OWNER}/{BRANCH}/{COMMIT}/{RUTA_ARCHIVO}.puml
```

Por ejemplo:
```
https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/d164f69b39ea5a5b125bf1cee13acd15718cd5a9/ejemplo.puml
```
#### Nota sobre repositorios privados

Si el archivo plantuml se encuentra en un repo privado, para acceder al raw se 
necesita de un token que se agrega al final del link en forma de query, por lo
que el link quedaría así:
```
https://raw.githubusercontent.com/{OWNER}/{REPO}/{COMMIT}/{RUTA_ARCHIVO}.puml?token={TOKEN}
```
Estos tokens se generan por cada commit, por lo que para que nuestra solución
perdure hay que cambiar el campo `BRANCH` por el hash del commit 
correspondiente (y acordarse de irlo actualizando junto con el token).

Podés encontrar al final del readme un par de mini guías de 
[cómo acceder al hash de un commit](#cómo-acceder-al-hash-de-un-commit) y
[cómo acceder al raw de un archivo](#cómo-acceder-al-raw-de-un-archivo)

### Paso 2

Vamos a usar el servicio de [Proxy](https://plantuml.com/server) de PlantUML
para conseguir el link que vamos a insertar en nuestro README.md
```
http://www.plantuml.com/plantuml/proxy?cache=no&src={LINK_RAW}
```
Por ejemplo:
```
http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/d164f69b39ea5a5b125bf1cee13acd15718cd5a9/ejemplo.puml
```
### Paso 3

Pegar esa URL como imagen en el README.md, en formato Markdown:
```
![texto alternativo]({LINK_PLANTUML})
```

Por ejemplo:
```
![ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/d164f69b39ea5a5b125bf1cee13acd15718cd5a9/ejemplo.puml)
```
El resultado es el que está 
[al principio de este readme](#dds-plantuml-ejemplo).

## Cómo acceder al hash de un commit

Se puede acceder al hash desde consola o desde GitHub.

### Acceder al hash desde la consola

Ejecutar `git log`, desplazarse con las flechas hasta encontrar el commit
correcto y copiar su hash. Se sale con 'q'.

Por ejemplo:
```make
commit 7c99976dbc44f1a1d6eb617722e8e2ff693c40cb # <--- Este código raro es el hash
Author: Agustin Ranieri <aguseranieri@gmail.com>
Date:   Sun Apr 25 18:02:18 2021 -0300

    agrego puml ejemplo
```

### Acceder al hash desde GitHub

1. Ir a la sección "commits" del repo:

![image](https://user-images.githubusercontent.com/39303639/119248270-6b870080-bb66-11eb-8787-98c5e91818d1.png)

2. Buscar el commit y hacer click para copiar el portapapeles:

![image](https://user-images.githubusercontent.com/39303639/119248383-2adbb700-bb67-11eb-9a2e-247d17305698.png)

Esto nos obtiene el mismo hash que mediante el otro método:
```
7c99976dbc44f1a1d6eb617722e8e2ff693c40cb
```

## Cómo acceder al raw de un archivo

1. Ir a la sección "commits" del repo:

![image](https://user-images.githubusercontent.com/39303639/119248270-6b870080-bb66-11eb-8787-98c5e91818d1.png)

2. Buscar el commit y hacer en `<>` para ver el estado del repo en ese commit:

![image](https://user-images.githubusercontent.com/39303639/119248857-54e2a880-bb6a-11eb-84fe-cbd8631bc1e0.png)

3. Moverse hacia el archivo en cuestión y hacer click en `View raw`:

![image](https://user-images.githubusercontent.com/39303639/119248910-cfabc380-bb6a-11eb-95de-d1c5bd3c3054.png)

Esto nos va a llevar al mismo link que vamos a necesitar para el [paso 1](#paso-1).

## Créditos

Este método fue extraído del siguiente comentario en StackOverflow: https://stackoverflow.com/a/32771815/14089741