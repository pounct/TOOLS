<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  
</head>
<body>

  <h1>Comandos Git y GitHub Útiles</h1>

  <h2>Configuración Inicial</h2>
  <p>Configurar nombre de usuario y correo electrónico</p>
  <pre><code>git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"</code></pre>

  <p>Ver configuración global</p>
  <pre><code>git config --global --list</code></pre>

  <h2>Gestión de Repositorios Locales</h2>
  <p>Inicializar un nuevo repositorio</p>
  <pre><code>git init</code></pre>

  <p>Clonar un repositorio existente</p>
  <pre><code>git clone &lt;url_del_repositorio&gt;</code></pre>

  <p>Ver el estado de los archivos modificados</p>
  <pre><code>git status</code></pre>

  <p>Agregar cambios para el próximo commit</p>
  <pre><code>git add &lt;nombre_del_archivo&gt;  # Agregar un archivo específico
git add .                     # Agregar todos los archivos modificados</code></pre>

  <p>Hacer commit de los cambios</p>
  <pre><code>git commit -m "Mensaje del commit"</code></pre>

  <h2>Gestión de Ramas</h2>
  <p>Crear una nueva rama</p>
  <pre><code>git branch &lt;nombre_de_la_rama&gt;</code></pre>

  <p>Cambiar a una rama específica</p>
  <pre><code>git checkout &lt;nombre_de_la_rama&gt;</code></pre>

  <p>Crear y cambiar a una nueva rama</p>
  <pre><code>git checkout -b &lt;nombre_de_la_nueva_rama&gt;</code></pre>

  <p>Fusionar una rama en la rama activa</p>
  <pre><code>git merge &lt;nombre_de_la_rama_a_fusionar&gt;</code></pre>

  <p>Eliminar una rama local</p>
  <pre><code>git branch -d &lt;nombre_de_la_rama&gt;</code></pre>

  <h2>Gestión de Repositorios Remotos (GitHub)</h2>
  <p>Agregar un repositorio remoto</p>
  <pre><code>git remote add origin &lt;url_del_repositorio&gt;</code></pre>

  <p>Ver repositorios remotos</p>
  <pre><code>git remote -v</code></pre>

  <p>Subir cambios a un repositorio remoto</p>
  <pre><code>git push -u origin &lt;nombre_de_la_rama&gt;</code></pre>

  <p>Obtener cambios desde un repositorio remoto</p>
  <pre><code>git pull origin &lt;nombre_de_la_rama&gt;</code></pre>

  <p>Crear una nueva rama en el repositorio remoto</p>
  <pre><code>git push origin &lt;nombre_de_la_nueva_rama&gt;</code></pre>

  <h2>Gestión de Cambios Locales</h2>
  <p>Deshacer cambios locales en un archivo específico</p>
  <pre><code>git checkout -- &lt;nombre_del_archivo&gt;</code></pre>

  <p>Deshacer todos los cambios locales</p>
  <pre><code>git checkout .</code></pre>

  <p>Volver a un commit específico (PRECAUCIÓN: Usar con cuidado)</p>
  <pre><code>git reset --hard &lt;código_del_commit&gt;</code></pre>

  <p>Ver historial de commits</p>
  <pre><code>git log</code></pre>

</body>
</html>
