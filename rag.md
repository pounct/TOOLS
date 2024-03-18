
# Generación Aumentada por Recuperación
# Retrieval Augmented Generation  (RAG)
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


<body>
<h1>Introducción</h1>

<p>RAG (Generación Aumentada por Recuperación) es un marco que combina la generación de lenguaje natural (NLG) con la recuperación de información (IR) para mejorar la precisión y la fluidez de la salida del modelo. Este documento describe los bloques constitutivos de RAG.</p>

<h2>Paso 1: Ingestión de fuentes de datos</h2>

<p>El primer paso es ingerir diferentes fuentes de datos en una base de datos para formar una capa de contexto. Esto puede incluir:</p>

<ul>
  <li>Documentos: PDF, Word, Excel, etc.</li>
  <li>Multimedia: Audio, video, etc.</li>
</ul>

<p>Es importante seleccionar cuidadosamente los documentos relevantes para la entrada del usuario para que el LLM solo responda en función del contexto.</p>

<h2>Paso 2: Dividir en fragmentos</h2>

<p>Las  datos brutos se dividen en fragmentos más pequeños antes de pasarlos a un modelo de incrustación. Esto se hace por dos razones:</p>

<ol>
  <li>Los modelos de incrustación tienen restricciones de longitud de entrada.</li>
  <li>Permite un control preciso sobre la información inyectada como contexto.</li>
</ol>

<h2>Paso 3: Incrustación de contenido</h2>

<p>Los fragmentos se transforman en representaciones vectoriales. Esto permite construir un motor de búsqueda semántico con una base de datos local. La consulta (convertida en vector) se compara con los vectores de documentos para seleccionar solo los documentos similares a la consulta.</p>

<h2>Paso 4: Almacenamiento en una base de datos vectorial (VDBMS)</h2>

<p>Las incrustaciones se pueden almacenar para una recuperación eficiente en VDBMS como:</p>

<ul>
  <li>Pinecone: [https://www.pinecone.io/](https://www.pinecone.io/)</li>
  <li>ChromaDB: [https://www.trychroma.com/](https://www.trychroma.com/)</li>
</ul>

<h2>Paso 5: Aplicación RAG</h2>

<p>La aplicación RAG permite:</p>

<ol>
  <li>Ingresar la consulta del usuario.</li>
  <li>Transformar la consulta en una representación vectorial.</li>
  <li>Consultar el VDBMS para realizar una búsqueda semántica.</li>
  <li>Recuperar documentos relevantes al contexto de la consulta.</li>
  <li>Inyectar el contenido contextual en el prompt.</li>
  <li>Presentar el prompt al LLM para generar una respuesta.</li>
  <li>Recuperar la respuesta del LLM.</li>
  <li>Enviar la respuesta al usuario.</li>
</ol>

<h2>Consideraciones adicionales</h2>

<ul>
  <li>Se pueden usar modelos de incrustación pre-entrenados como `ada` para simplificar la incrustación de contenido.</li>
  <li>La elección del VDBMS depende del tamaño del corpus de datos, el rendimiento y el presupuesto.</li>
  <li>La aplicación RAG se puede implementar con frameworks como TensorFlow, PyTorch o FastAPI.</li>
</ul>

<h2>En resumen, los bloques constitutivos de RAG son:</h2>

<ul>
  <li>Ingestión de datos</li>
  <li>División en fragmentos</li>
  <li>Incrustación de contenido</li>
  <li>Almacenamiento en una VDBMS</li>
  <li>Aplicación RAG</li>
</ul>

</body>
