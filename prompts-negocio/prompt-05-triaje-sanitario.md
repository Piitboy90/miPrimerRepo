## PROMPT 05 – TRIAJE SANITARIO 

## SECTOR 
CENTRO DE SALUD 
 
## PROBLEMA QUE RESUELVE 
Categorizamos alto volumen de consultas en centro de salud primario, y generamos con eficiencia un primer informe eficiente para optimizar recursos. 
 
## CONVERSACIÓN A ANALIZAR 
```` 
 
— Triaje: Hola, buenos días. Antes de nada, ¿me dices tu nombre y apellidos?
— Paciente: Sí, claro, Javier Martín López.
 — Triaje: Vale, Javier, ¿y tu número de la Seguridad Social lo tienes a mano?
— Paciente: Sí, es 12/3456789/01.
— Triaje: Perfecto. Ahora cuéntame, ¿qué te pasa?
— Paciente: Pues desde anoche estoy fatal, con mucho dolor de garganta y fiebre.
— Triaje: ¿Te has tomado la temperatura en casa?
— Paciente: Sí, esta mañana tenía casi 39.
 — Triaje: ¿Te cuesta respirar o tragar?
— Paciente: Respirar no, pero tragar me duele muchísimo.
— Triaje: Vale, te voy a tomar ahora la temperatura y la tensión, y en cuanto pueda te llama el médico.

````
 
## PROMPT COMPLETO 
 
Instrucciones: 
 
* Analiza la conversación detenidamente como especialista médico de urgencias. 
* Extrae nombre, apellidos y nº seguridad social del paciente 
* Extraemos los 3 puntos clave que comunique el paciente con respecto a los motivos de su consulta, para incluir en el primer informe médico. 
* Categorizamos la gravedad de la dolencia, del 1 al 3, siendo 1(dolencia baja que requiera solo de revisión y un tratamiento), 2 (dolencia media que requiera ingreso hospitalario para observación), 3 (dolencia grave que requiera intervención quirúrgica de urgencia). 
* Generamos primer informe de especialista médico de cara a la próxima revisión. 
* Los datos personales deben ser anonimizados en el output final antes de compartir el informe. 
* Incluye al final del informe la nota: “Este informe es orientativo y debe ser validado por un profesional médico.” 
* Devuelve JSON, con datos personales, 3 puntos clave, categoría de la gravedad y finalmente informe médico. 
 
## OUTPUT DEVUELTO 
 
````
{ "datos_personales": { "nombre": "J***", "apellidos": "M***** L****", "numero_seguridad_social": "**/*******/*1" },
"3_puntos_clave": [ "Dolor intenso de garganta iniciado desde la noche anterior.", "Fiebre alta referida por el paciente, con temperatura aproximada de 39 °C en domicilio.", "Dolor importante al tragar, sin dificultad respiratoria asociada." ],
"categoria_gravedad": { "nivel": 1, "descripcion": "Dolencia baja que requiere revisión médica y posible tratamiento, sin signos referidos de compromiso respiratorio ni indicios de urgencia quirúrgica." },
"informe_medico": "Paciente atendido en triaje por cuadro agudo de odinofagia intensa y fiebre alta de inicio reciente. Refiere temperatura domiciliaria cercana a 39 °C y dolor importante al tragar. Niega dificultad respiratoria. Se recomienda valoración médica prioritaria en consulta para exploración orofaríngea, control de constantes y determinación de tratamiento sintomático o etiológico según hallazgos clínicos. Este informe es orientativo y debe ser validado por un profesional médico." } 

````
 
 
 
## POR QUÉ FUNCIONA 
* Se aplican delimitadores para separar conversación de las instrucciones, combinando inferring y sumarizing.  
* Permite categorizar volumen de consultas generando primer informe y reduciendo listas de espera. 
* Aplicamos JSON ya que nos permite integrarlo en el sistema hospitalario.
