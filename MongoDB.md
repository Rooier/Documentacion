# MONGODB

|  Comando  |  Descripcion  |
|:---------:|:--------------|
|  help()   |  muestra mensaje en consola  
db.stats()			|	muestra las estadisticas de la base de datos (Objetos, tamaño, almacenamiento, indices...)
use {database}		|	crea una nueva base de datos o cambia a esa base de datos.
show bds 			|	listar las bases de datos existentes
db 					|	muestra la base de datos en uso
db.dropDatabase()	|	Elimina una base de datos **Revisar que base de datos esta en uso para eliminar correctamente.
db.createCollection("nombre_colleccion") 	|	crear colleccion simple en la base de datos
db.createCollection("nombre_colleccion", {capped : true, size : sizeLimit, max : documentLimit })	|	crear coleccion capada  - Restringe el tamaño y el numero de documentos que se insertaran en la coleccion. Existe una propiedad que permite eliminar los docs mas antiguos para dejar espacio a los nuevos documentos.
db.createCollection("coleccion_capada", {capped:true, max:1, size:200})
db.coleccion_capada.insertMany([{"id":1, status:"Activo"},{"id":2, status:"Retenido"},{"id":3, status:"Pendiente"}])

Al realizar el insert de varios registros, por la condicions de max 1, solo quedara el ultimo registro

db.[nombre_coleccion].drop() 	|	elimina la coleccion  , devuelve true en caso de exito

db.collectionName.insertOne({codigo:"A0001", cantidad: 200, estado:"Acivo"});		|		Insertar un registro a la colleccion

db.coleccion_test.insertMany([{codigo:"A0002", cantidad: 50, estado:"Acivo"},{codigo:"A0003", cantidad: 0, estado:"Inactivo"},{codigo:"A0005", cantidad: 500, estado:"Acivo"}])


find()			|		Buscar toda la coleccion

update o UpdateOne 	|	
updateMany key set



deleteOne


renameCollection
