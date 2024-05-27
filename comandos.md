# Clonar el repositorio
git clone https://github.com/DavidBernalGonzalez/practicaGit.git
cd practicaGit

# Visualizar las ramas
git branch -a

# Cambiar a la rama practica01
git checkout practica01

# Editar archivos en practica01
cd practica01
# Editar archivos
git status

# Hacer commit
git add .
git commit -m "Editados los archivos en la carpeta practica01"

# Crear y cambiar a una nueva rama
git checkout -b practica1_NIEVAS_CRISTIAN

# Crear y modificar archivo en la nueva rama
cd ..
echo "Contenido inicial" > practica1_NIEVAS_CRISTIAN.txt
git add practica1_NIEVAS_CRISTIAN.txt
git commit -m "Añadido el archivo practica1_NIEVAS_CRISTIAN.txt con contenido inicial"

# Editar el archivo con nombre y apellidos
echo "Nombre Apellidos" > practica1_NIEVAS_CRISTIAN.txt
git add practica1_NIEVAS_CRISTIAN.txt
git commit -m "Actualizado el archivo practica1_NIEVAS_CRISTIAN.txt con nombre y apellidos"

# Cambiar el repositorio remoto
git remote remove origin
git remote add origin https://github.com/TU_USUARIO/practicaGit.git
git push -u origin practica1_NIEVAS_CRISTIAN

# Volver a la rama practica01
git checkout practica01

# Hacer merge con la rama practica1_NIEVAS_CRISTIAN
git merge practica1_NIEVAS_CRISTIAN
