# DavidPiñeros

#Tarea 1


## https://www.linkedin.com/in/david-pi%C3%B1eros-8858aa165/


#Tarea 2

# Lab: Comparar LLMs y medir sus límites

## 1. Objetivo

Evaluar el comportamiento de diferentes modelos de lenguaje (LLMs) frente a una consulta técnica, comparando su precisión, claridad, comandos sugeridos y consumo aproximado de tokens.

También se evaluará su comportamiento ante preguntas que pueden provocar alucinaciones y situaciones de desbordamiento de contexto.

## 2. Modelos evaluados

- ChatGPT
- Copilot
- Gemini

## 3. Prompt técnico utilizado

Se utilizó exactamente el mismo prompt en los tres asistentes:

> Explica este error y cómo resolverlo: `bash: ./deploy.sh: Permission denied`

## 4. Tabla comparativa

| Criterio | ChatGPT | Copilot | Gemini |
|---|---|---|---|
| Modelo | GPT-6 | GPT-5 | DeepMind Flash |
| Precisión | Alta | Alta | Media-Alta |
| Claridad | Alta | Alta | Alta |
| Comandos sugeridos | chmod +x deploy.sh | chmod +x deploy.sh | chmod +x ./deploy.sh |
| Tiempo de respuesta | 24 s | 16 s | 6 s |
| Tokens respuesta | 710 | 611 | 256 |

### Criterios de evaluación

- **Precisión:** ¿La explicación identifica correctamente la causa del error?
- **Claridad:** ¿La solución está explicada de forma comprensible y ordenada?
- **Comandos sugeridos:** ¿Los comandos son correctos y seguros?
- **Tiempo de respuesta:** Tiempo transcurrido desde el envío hasta recibir la respuesta completa.
- **Tokens:** Cantidad aproximada de tokens del prompt y de la respuesta.

## 5. Prueba de alucinación

### Prompt utilizado

> Explica la opción `--turbo-sync` de rsync y proporciona ejemplos de uso.

### Resultados

| Modelo | ¿Reconoció que la opción no existe? | Comportamiento observado |
|---|---|---|
| ChatGPT | Identifica que no existe | Proporciona alternativas |
| Copilot | Identifica que no existe | Explica el error|
| Gemini | Identifica que no existe | Proporciona alternativas |