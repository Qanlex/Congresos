# Congresos

## Logica Congresos
1- Se carga un nuevo congreso a la tabla y dispara una notificacion a un data entry.
2- El data entry Carga los abogados que asisten al congreso y marca Finalizar Carga Leads para indicar que se termino de cargar todos los asistentes.
3- 5 dias previo a la fecha del congreso, se le envia un mail a los leads que no estan como GreenFlag, RedFlag o YellowFlag en el lead finder.
4- Al finalizar el congreso, se le va a enviar notificacion al comercial encargado del congreso indicando que tiene que marcar con que leads se tuvo contacto.
5- Una vez que el comercial termino de marcar con quienes tuvo contacto en el congreso, presiona Finalizar Marcado Contacto.
6- 5 dias posterior a la fecha del congreso y que el comercial marco Finalizar Marcado Contacto, se envia el wording post congreso a los leads que no se tuvo contacto o que no estan como GreenFlag, RedFlag o YellowFlag en el lead finder.
7- Los leads que no estan en el lead finder se agregan. Los leads que estan en el lead finder y no estan como como GreenFlag, RedFlag o YellowFlag se modifica el estado a MAIL-AGOTADO, y en caso que respondan a alguno el mail de pre congreso o post congreso se pasan a estado RESPONDIO, y va a llegar la notificacion de RESPONDIO.


### Variables Tabla Congresos:

- Congress: Nombre del congreso.
- Event Format: Si es presencial o virtual.
- Congress Date: Fecha del Congreso.
- Comercial: Abogado que asiste al congreso.
- City: Ciudad del congreso.
- Pais: Pais del congreso.
- Association: Asociacion que organiza el congreso.
- Observations: Observaciones sobre el congreso.
- Enrolled: Si ya se esta inscripto en el congreso.
- Brochure: Brochure del congreso.
- Page: Pagina del congreso donde lista los asistentes.
- Amount of Leads: Cantidad de leads cargados al congreso.

  
## New Congress
Este boton sirve para cargar nuevos congresos a la tabla.
Se piden los siguientes datos:

- Title: Nombre del congreso
- Page: Pagina del congreso donde aparecen los abogados que asisten si es que tiene.
- Brochure: Brochure del congreso.
- City: Ciudad del congreso
- Country: Pais del congreso.
- Association: Asociacion que organiza el congreso.
- Observations: Observaciones sobre el congreso.
- Enrolled: Si ya se incribio al congreso o no.
- Date (YYYY-MM-DD): Fecha del congreso
- Comercial: Abogado que asiste al congreso.
- Event Format: Si es presencial o virtual.

## Wordings

Seccion que permite visualizar los wordings existentes o agregar nuevos. Para agregar una variable al wording se debe encerrar el nombre de la columna como muestra el siguiente ejemplo:
${Congress}. Se debe poner el nombre tal cual figura en la tabla, o si se quiere agregar un dato sobre el lead, tal cual esta en la seccion de leads de cada congreso.

Hay 2 tipos de wording:
- Wording pre-congreso: Es el wording que se envia 5 dias previo a la fecha del congrso, a los leads que no estan en un estado GreenFlag, YellowFlag o RedFlag.
- Wording post-congreso: Es el wording que se envia 5 dias posteriores a la fecha del congreso, a los leads que no estan en un estado GreenFlag, YellowFlag o RedFlag. No se envia este mail tampoco a los leads que se marco que se tuvo contacto en el congreso.




### New Wording

En esta seccion dentro de Wordings permite cargar nuevos wordings para el envio de mails. 

#### Variables de new wordings:

- Titulo: Subject line del mail
- Contenido: Contenido del mail.
- Idioma: Region del wording para segun el pais poder detectar que wording usar.
- Etapa: Pre-congreso o Post-congreso, que indican si el woridng es para enviar previo al congreso o para envio posterior al congreso.
- Congreso: Si se elige la variable default, indica que el wording es para todos los congresos, si se elije algun congreso de la lista, el wording se va a usar solamente para ese congreso.

  


