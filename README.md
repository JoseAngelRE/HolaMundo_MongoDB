# "HOLA MUNDO" en MongoDB
Curso básico de MongoDB

[VIDEO CURSO](https://youtu.be/RDdiUHZECUE)

[PRESENTACIÓN](https://www.canva.com/design/DAES90LgnCs/tcmB6hPufHJ7355THFXxlQ/view?utm_content=DAES90LgnCs&utm_campaign=designshare&utm_medium=link&utm_source=publishsharelink)

## PUNTOS PRINCIPALES

MongoDB es:

- Open Source
- NoSQL (Not only SQL)
- Documents Oriented
- Schema Less
- Scale Out

## DOCUMENTOS

Son la unidad básica y se representa en formato JSON:

```javascript
{
  "_id": "5cf0029caff5056591b0ce7d",
  "firstname": "Jane",
  "lastname": "Wu",
  "address": {
    "street": "1 Circle Rd",
    "city": "Los Angeles",
    "state": "CA",
    "zip": 90404
  },
  "hobbies": ["surfing", "coding"]
}
```

### COLECCIÓN

Son agrupaciones de documentos. No nos imponen un esquema o estructura rígida para guardar nuestra información.

### BASE DE DATOS

Contenedores de colecciones.

### CLUSTER

Contiene las bases de datos.

De forma un poco mas gráfica podríamos verlo de la siguiente manera:

CLUSTER > BASE DE DATOS > COLECCIÓN > DOCUMENTOS

## PRIMEROS PASOS

Como ejemplo en todo el curso haremos una representación de una ferretería.

### ¿Cómo entrar a MongoDB?

+ Abrir la terminal para iniciar el servidor:

`> mongod`

+ Dejemos abierta la anterior y abriremos una nueva:

`> mongo`

Desde esta segunda terminal abierta haremos todo lo demás.

## Insertar

+ Ver las bases de datos.

`> show dbs`

+ Base de datos actual.

`> db`

+ Hacer una nueva base de datos.

`> use ferreteria`

+ Insertar una colección.

`> db.createCollection("mercancia")`

+ Mostrar las colecciones.

`> show collections`

+ Insertar un documento a una colección.

`> db.mercancia.insert({"nombre": "escoba", "precio": 150})`

+ Insertar varios documentos a una coleccion.

`> db.mercancia.insert([{"nombre": "escoba", "precio": 150},{"nombre": "pala", "precio": 200}])`

## Buscar dentro de las colecciones

* Forma normal.

`> db.mercancia.find()`

* Forma ordenada.

`> db.mercancia.find().pretty()`

* Buscar por algun atributo específico.

`> db.mercancia.find({"nombre": "escoba"}).pretty()`

* Contar los documentos que hay dentro de alguna coleccion.

`> db.mercancia.count()`

* Mostrar con un límite.

`> db.mercancia.find({}).limit(2)`

* Ordenarlo.

`> db.coleccion.find({"precio": 200}).sort({nombre: 1})`

## Actualizar

* Actualizando todo el documento por otro.

`> db.mercancia.update({"nombre": "pala"}, {"fabricante": "truper"})`

* Actualizando el documento sin eliminar los demás datos.

`> db.mercancia.update({"nombre": "escoba"}, {$set: {"fabricante": "truper"}})`

## Eliminar 

* Eliminar documentos.

`> db.mercancia.remove({"nombre": "escoba"})`

* Eliminar colección.

`> db.mercancia.drop()`

* Eliminar base de datos.

`> db.dropDatabase()`
 
## Cerrar MongoDB

* Cerrar la terminal en la que trabajamos.

`> exit`

Ahora ya se puede cerrar la ventana.

En la otra terminal nos aparecerá que se cerró la conexión. Basta con teclear "Control C" y estará todo terminado.








