# dds-plantuml-ejemplo
Ejemplo de uso de la herramienta plantUML en un readme de GitHub

![ejemplo](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/RaniAgus/plantuml-ejemplo/master/ejemplo.puml)

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

Al principio del README se encuentra insertada esta misma imagen.

## Requisitos

Esta solución funciona solamente para repositorios públicos, ya que el proxy de PlantUML necesita permisos para acceder al raw del archivo puml desde fuera.

## Créditos

Este método fue extraído del siguiente comentario en StackOverflow: https://stackoverflow.com/a/32771815/14089741