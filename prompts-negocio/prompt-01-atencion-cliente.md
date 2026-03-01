# Prompt 01 — Análisis de reseña negativa para Atención al Cliente

## Sector
E-commerce / Electrónica

## Problema que resuelve
Detectar automáticamente reseñas negativas, extraer términos clave 
y generar una respuesta conciliadora lista para usar en atención al cliente.

## Prompt completo

RESEÑA EXTRAÍDA DE www.backmarket.es
```Me parece ridículo que todavía vendan un teléfono insignia 
con una pantalla de 60 Hz. Debería haber sido 120 Hz durante años.```

Instrucciones:
- Obtén los 3 términos/palabras clave que determinan el contexto de la frase.
- Analiza si hay alguna referencia negativa. Responde sí o no. Si es sí, muestra la palabra.
- Esta reseña va dirigida al departamento de atención al cliente. 
  Genera una respuesta conciliadora que no supere los 250 caracteres.
- Devuelve toda la información en formato JSON.

## Output obtenido

{
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

## Por qué funciona

Permite extraer la información relevante de cara a una solución concreta.
Nos enfocamos en el contenido a través de las palabras clave.
Trabajamos para mantener el vínculo con el cliente.
