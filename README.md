# dds-plantuml-ejemplo
Ejemplo de uso de la herramienta [plantUML](http://www.plantuml.com/plantuml/uml/SoWkIImgAStDuU9oICrB0J80) en un readme de GitHub

![guia](https://user-images.githubusercontent.com/677436/115094178-08fd6d80-9ef3-11eb-8bea-ce64f9c34eef.png)

## Limitaciones

Esta solución funciona solamente para repositorios públicos, ya que el proxy de PlantUML necesita permisos para acceder al raw del archivo puml desde fuera.

## Créditos

Este método fue extraído del siguiente comentario en StackOverflow: https://stackoverflow.com/a/32771815/14089741

## Pasos a seguir

### Paso 1

Obtener la URL hacia el raw del archivo PlantUML, la cual tiene el formato:
```
https://raw.githubusercontent.com/<owner>/<repo>/<branch>/<path_al_archivo>.puml
```

Por ejemplo:
```
https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/master/ejemplo.puml
```

### Paso 2

Vamos a usar el servicio de [Proxy](https://plantuml.com/server) de PlantUML
para conseguir el link que vamos a insertar en nuestro README.md
```
http://www.plantuml.com/plantuml/proxy?cache=no&src=<link>
```
Por ejemplo:
```
http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/master/ejemplo.puml
```
### Paso 3

Pegar esa URL como imagen en el README.md, en formato Markdown:
```
![<nombre-alternativo>](<link>)
```

Por ejemplo:
```
![ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/master/ejemplo.puml)
```

Resultado:

![ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/master/ejemplo.puml)
