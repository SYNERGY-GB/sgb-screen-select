# SGB-screen-selection
### Propósito

Esta pantalla es una vista que permite enlistar un conjunto de objetos que representen una gama de opciones. La misma permite que la selección se limite a un solo elemento o se pueda realizar una multiselección. Esto permitiría que la(s) opcion(es) seleccionadas sean tomadas para otra vista.

### Datos esperados

Se debe recibir un objeto con el título de la pantalla, la instrucción, descripciones y una lista de opciones.

### Datos obligatorios
* **options**:
	* **text**:  Texto de la opción
	* **image**: Imagen del avatar que acompañaría la correspondiente opción
	* **checked**: Identificador para las opciones seleccionadas

### Datos opcionales

* **tabtitle**: Título identificador de la vista
* **desc1**: Primer párrafo descriptivo
* **desc2**: Segundo párrafo descriptivo
* **options**:
	* **value**: Identificador de la opción
	* **url**: Texto secundario de la opción
	* **instruction**: Instrucción sobre la selección de opciones

### Ejemplo JSON

```json
data = {

	"tabtitle":"Change Country",
	"instruction":"Instruction",
	"desc1" : "Here goes the first description, for people to understand that this is a screen for something relevant, which I still don't know.",
	"desc2" : "Here goes the first description, for people to understand that this is a screen for something relevant, which I still don't know.",
	"options" : [
    {
    	"value":1,
        "text": "Alemania",
        "image": "https://upload.wikimedia.org/wikipedia/commons/a/a9/Flag_of_Germany_as_seen_in_Tagesschau.jpg",
        "url":"amazon.de",
        "checked":false
    },
    {
    	"value":2,
        "text": "Venezuela",
        "image": "http://tururutururu.com/wp-content/uploads/2013/08/venezuela-8-stars-5-x-3-flag-4064-pekm1000x650ekm-720x375.jpg",
        "url":"amazon.ve",
        "checked":false
    }
	]
}; 
```

### Parámetros de la pantalla

* **type**: Sting indicador del tipo de selección que se va a permitir en la vista. 'single' o 'multi'

### Diseño

Indistintamente del tipo de selección elegido, el diseño de la pantalla se mantiene. La variación es en la cantidad de opciones que se marcarían con un check dependiento si es uniselección o multiselección.

### Opción 'single'

![alt text](http://i325.photobucket.com/albums/k362/gbsojo/single-selection_zpsfpcf3va0.png "Single Selection")

### Opción 'multi'

![alt text](http://i325.photobucket.com/albums/k362/gbsojo/multiselection_zps0qop9kfh.png "Multiselection")

