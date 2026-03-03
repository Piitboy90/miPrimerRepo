## PROMPT 04 – ANALISIS VENTAS 

 

## SECTOR 

Ventas 

 

## PROBLEMA QUE RESUELVE 

Identificamos en qué fase de venta se encuentra la conversación y sugerimos una respuesta adecuada que permita lograr éxito de venta final. 

 

## EJEMPLO CONVERSACIÓN VENTA 

```` 

Escenario: Venta de un smartwatch en una tienda de tecnología. 

Vendedor: ¡Hola! Bienvenido/a. Veo que estás mirando la sección de relojes inteligentes, ¿buscas algo para uso diario o más enfocado en deporte? 

Cliente: Más bien para deporte, pero que también me sirva para el día a día. 

Vendedor: Perfecto, entonces te recomendaría este modelo. Tiene GPS integrado, mide frecuencia cardíaca en tiempo real y la batería dura hasta 10 días. Además, su diseño es elegante, así que combina bien con ropa casual o de oficina. 

Cliente: Suena bien, pero me preocupa que sea complicado de usar. 

Vendedor: Entiendo tu preocupación. Este modelo es muy intuitivo: solo necesitas sincronizarlo con tu móvil una vez, y después todo se maneja desde la pantalla táctil. Incluso puedes recibir notificaciones y contestar llamadas sin sacar el teléfono. 

Cliente: ¿Y el precio? 

Vendedor: Ahora mismo está en oferta: de 199 € a 159 €, con garantía de dos años y la posibilidad de devolverlo en 30 días si no te convence. 

```` 

 

## PROMPT COMPLETO 

Instrucciones: 

- Analiza como director en ventas la conversación e identifica si tenemos potencial cliente. Determina la fase de venta: Interés inicial / Consideración / Objeción / Listo para cerrar 
- Si determinas que el cliente no está interesado, genera respuesta conciliadora que incite a una próxima oportunidad de venta. 
- Si determinas que es cliente potencial, genera respuesta adecuada que cierre la venta y que además cree un vínculo de confianza y fidelidad con la marca. 
- Devuelve JSON estructurado, fase de venta, probabilidad de cierre, respuesta sugerida. 

 

## OUTPUT DEVUELTO 

 
````
{ 

  "fase_de_venta": "Objeción", 

  "probabilidad_de_cierre": "Alta", 

  "respuesta_sugerida": "Es una muy buena pregunta. Teniendo en cuenta que buscas un smartwatch para deporte y uso diario, este modelo encaja muy bien contigo por su equilibrio entre facilidad de uso, funciones avanzadas y diseño. Además, ahora mismo lo tienes rebajado a 159 €, con 2 años de garantía y 30 días de devolución, así que puedes probarlo con total tranquilidad. Si quieres, te lo dejamos configurado ahora mismo para que te lo lleves listo y veas desde el primer día lo fácil que es usarlo." 

} 
````
 

 

## POR QUÉ FUNCIONA 

 

- Se aplican delimitadores para separar la conversación de las instrucciones, lógica condicional para dos escenarios distintos de respuesta, y campos específicos definidos en el JSON. 
- Resuelve el problema de escalar el análisis comercial sin depender de un director de ventas para cada conversación.
- El JSON permite integrarlo directamente a un sistema de seguimiento de leads. 
