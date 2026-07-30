Me planto con algo más que casi se me olvida. Estoy registrando cómo manejar desde la terminal el flujo de trabajo propio de este sistema de configuración. Voy a escribir el tipo de comandos usados para ello, junto con la función de los mismos. Primero, te tienes que encontrar en la terminal en la carpeta asignada al vault que estás usando.
	1. git init <utilizado para iniciar el repositorio en la carpeta en que te encuentras>
	2. git clone {{repository-url}} <>
	3. git branch <utilizado para conocer la branch en que te encuentras. Es decir, la división espacial desde la que modificas el repositorio. Es, a modo de símil, cómo divides el material de Soporte Vital Avanzado: en una mochila de circulatorio y en una mochila de respiratorio. De manera predeterminada te encuentras en *main*.>
	4. git branch {{branch-name}} <utilizado para crear una nueva branch.>
	5. git switch {{branch-name}} <utilizado para cambiar la branch desde la que modificas el texto>
	6. realiza cualquier cambio en el vault, teniendo en cuenta no modificar carpetas, archivos o notas que otros usuarios puedan modificar. En el caso de ocurrir esto último, se produciría una discordancia entre las versiones usadas y sería necesario "fusionarlas", lo que sería hacer *merge*.
	7. git add . <utilizado para añadir cualquier modificación que hagas en el vault>
	git pull <utilizado para igualar las versiones de aquello que está escrito en el repositorio y evitar que se produzcan discordancias>
	8. git commit -m "mensaje sobre los cambios realizados"
	9. git config --global push.default current <para no especificar desde que branch estás subiéndolo>
	10. git push <utilizado para subir al repositorio los cambios realizados, dejando previsto el cambio de versiones para hacer una solicitud de revisión de *commit* en el repositorio de Github>
	11. usename + personal access token <en principio, no es necesario mientras estés autenticado con tu clave de SSH>
