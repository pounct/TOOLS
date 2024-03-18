
# Generación Aumentada por Recuperación (RAG)
- Consideremos que queremos preguntar al LLM sobre el contenido de un informe anual.

- Aunque el modelo es capaz de comprender las instrucciones en el prompt, no tiene idea de lo que ha sucedido después de la fecha de su entrenamiento.

- En concreto, es muy probable que el informe anual no haya sido incluido en el entrenamiento.

- En este caso, el resultado del LLM sería, en el mejor de los casos, inútil y, en el peor, incorrecto (lo que se conoce como "alucinación").

- Para corregir esta seria limitación, debemos ensamblar e inyectar un contexto generado dinámicamente en función de las entradas del usuario.

- Un ejemplo típico es cuando los datos almacenados por las organizaciones se utilizan como fuente de contexto para responder a las preguntas de los usuarios.

- Esta idea de recuperar e inyectar un contexto relevante para la consulta en un prompt para mejorar la generación de la respuesta se llama Generación Aumentada por Recuperación (RAG).

## En resumen, RAG:

- Combina la generación de lenguaje natural (NLG) con la recuperación de información (IR) para mejorar la precisión y la fluidez de la salida del modelo.
- Permite al LLM acceder a información externa y usarla para generar respuestas más completas e informativas.
- Reduce el riesgo de alucinaciones al proporcionar al LLM una base sólida de conocimiento en la que basarse.
