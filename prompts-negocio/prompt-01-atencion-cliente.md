# Prompt 01 — Análisis de reseña negativa para Atención al Cliente

## Sector
E-commerce / Electrónica

## Problema que resuelve
Detectar automáticamente reseñas negativas, extraer términos clave 
y generar una respuesta conciliadora lista para usar en atención al cliente.

## RESEÑA EXTRAÍDA DE www.backmarket.es
``Me parece ridículo que todavía vendan un teléfono insignia  
con una pantalla de 60 Hz. Debería haber sido 120 Hz durante años.´´´

## Prompt completo

Instrucciones:
- Obtén los 3 términos/palabras clave que determinan el contexto de la frase.
- Analiza si hay alguna referencia negativa. Responde sí o no. Si es sí, muestra la palabra.
- Esta reseña va dirigida al departamento de atención al cliente. 
  Genera una respuesta conciliadora que no supere los 250 caracteres.
- Devuelve toda la información en formato JSON.

## Output obtenido

```{
  "reseña": {
    "fuente": "www.backmarket.es",
    "terminos_clave": [
      "teléfono insignia",
      "pantalla 60 Hz",
      "120 Hz"
    ],
    "referencia_negativa": {
      "detectada": true,
      "palabra": "ridículo"
    },
    "respuesta_atencion_cliente": "Entendemos tu frustración y es totalmente válida. Tomamos nota de tu opinión sobre la pantalla. Si deseas, podemos orientarte hacia modelos que mejor se adapten a tus expectativas. ¡Estamos aquí para ayudarte!"
  }
}
````

## Por qué funciona

Se aplican delimitadores para separar el texto de las instrucciones, output estructurado en JSON para facilitar el procesamiento, audiencia específica definida y límite de caracteres en la respuesta. Combina Inferring y Summarizing en un único prompt
