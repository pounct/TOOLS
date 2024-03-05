Comandos Git y GitHub Útiles
Configuración Inicial
Configurar nombre de usuario y correo electrónico
bash
Copy code
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
Ver configuración global
bash
Copy code
git config --global --list
Gestión de Repositorios Locales
Inicializar un nuevo repositorio
bash
Copy code
git init
Clonar un repositorio existente
bash
Copy code
git clone <url_del_repositorio>
Ver el estado de los archivos modificados
bash
Copy code
git status
Agregar cambios para el próximo commit
bash
Copy code
git add <nombre_del_archivo>  # Agregar un archivo específico
git add .                     # Agregar todos los archivos modificados
Hacer commit de los cambios
bash
Copy code
git commit -m "Mensaje del commit"
Gestión de Ramas
Crear una nueva rama
bash
Copy code
git branch <nombre_de_la_rama>
Cambiar a una rama específica
bash
Copy code
git checkout <nombre_de_la_rama>
Crear y cambiar a una nueva rama
bash
Copy code
git checkout -b <nombre_de_la_nueva_rama>
Fusionar una rama en la rama activa
bash
Copy code
git merge <nombre_de_la_rama_a_fusionar>
Eliminar una rama local
bash
Copy code
git branch -d <nombre_de_la_rama>
Gestión de Repositorios Remotos (GitHub)
Agregar un repositorio remoto
bash
Copy code
git remote add origin <url_del_repositorio>
Ver repositorios remotos
bash
Copy code
git remote -v
Subir cambios a un repositorio remoto
bash
Copy code
git push -u origin <nombre_de_la_rama>
Obtener cambios desde un repositorio remoto
bash
Copy code
git pull origin <nombre_de_la_rama>
Crear una nueva rama en el repositorio remoto
bash
Copy code
git push origin <nombre_de_la_nueva_rama>
Gestión de Cambios Locales
Deshacer cambios locales en un archivo específico
bash
Copy code
git checkout -- <nombre_del_archivo>
Deshacer todos los cambios locales
bash
Copy code
git checkout .
Volver a un commit específico (PRECAUCIÓN: Usar con cuidado)
bash
Copy code
git reset --hard <código_del_commit>
Ver historial de commits
bash
Copy code
git log
Esta es una lista no exhaustiva, y hay muchos otros comandos y opciones útiles en Git y GitHub. Para obtener más información, consulta la documentación oficial de Git y GitHub.
