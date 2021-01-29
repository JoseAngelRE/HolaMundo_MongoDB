# "HOLA MUNDO" en MongoDB
Curso básico de MongoDB

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

De forma un poco mas gráfica podriamos verlo de la siguiente manera:

CLUSTER > BASE DE DATOS > COLECCIÓN > DOCUMENTOS

## PRIMEROS PASOS

