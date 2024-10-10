# Desplegar aplicación Pokedex en la nube.

En este documento encontrará el paso a paso de cómo despleglar o públicar la aplicación **Pokedex** en la nube 


## Paso l - crear repositorio en GitHub 
1. seleccionar **Nuevo repositorio** 
2. Ingresar el nombre de este 
3. Seleccionar **Público** o **privado**
## Paso ll - Subir el proyecto localmente
1. Abrir la terminal en el proyecto local 
2. Iniciar Git con el comando **git init**
3. Agregar los archivos con el comando **git add .**
4. Confirmar los cambios con el comando **git commit -m "initial commit"**
5. Enlazar repositorio local con GitHub con el comando **git remote ad origin + URL**
6. Subir los cambios con el comando**git push -u origin master**
## Paso lll - Instalar librerías y configurar
1. Instala la librería npm necesaria con npm install.
2. Configura los headers de seguridad en tu archivo **index.html** o **header.php:** 
- Permission-Policy: 
- X-Frame-Options: 
- Strict-Transport-Security: 
- Content-Security-Policy: 
3. Sube los cambios con el comando **git add ., git commit -m "Seguridad configurada"** y el comando **git push**

## Paso lV - Crear App Service en Azure 
1. Inicia sesión en Azure.
2. Haz clic en **Crear un recurso**
3. Selecciona **Web** y luego **Application Web Static**
4. Ingresa el nombre de la app (p. ej., "pokdek").
5. Selecciona el plan de tarifa adecuado.
6. Haz clic en **Crear**

## Paso V - Enlazar con GitHub
1. En la sección **Deployment** de tu App Service.
2. haz clic en **Configuración de origen**
3. Selecciona **GitHub**-
4. Autentica con tu cuenta de GitHub.
5. Selecciona el repositorio **pokdek**
6. Selecciona la rama **master**
7. Haz clic en **Guardar**



## PASO Vl - Verificar
1. Espera a que Azure deploye tu aplicación.
2. Verifica que la aplicación esté funcionando correctamente.
3. Verifica que los headers de seguridad estén configurados correctamente.