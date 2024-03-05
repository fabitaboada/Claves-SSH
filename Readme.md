# 1.  
Tenemos que tener instalado SSH.  
Una vez hecho esto, generamos una clave con el comando:  
ssh-keygen  
Una vez ejecutado el comando, nos dirá que guardará esta clave en una ruta . Podemos también configurar una frase de seguridad.  

# 2.
En la carpeta en la que nos ha generado las claves, se encuentran la clave pública y la privada. (id_rsa.pub) y (id_rsa).  
Debemos compartir nuestra clave pública.  
Para ello empleamos el siguiente comando:  
ssh-copy-id [nombre_usuario]@[ip_compañero]  
Con esto podremos conectarnos a la máquina de un compañero empleando el siguiente comando:  
ssh [nombre_usuario]@[ip_usuario]  

# 3.    
Para crear una clave para github, nos vamos a settings en nuestra cuenta y al apartado de ssh. Una vez ahí, pulsamos add SSH key y nos mostrará un cuadro para introducir nuestra clave. Tenemos que meter nuestra clave pública ubicada en la carpeta oculta que se ha creado al generar la clave.  

# 4.  
Para añadir el repositorio con ssh, utilizaremos el siguiente comando:  
ssh -T git@github.com  
ssh clone git@github:fabitaboada/[Claves-SSH].git  

Finalmente hacemos un git add y un push:  
git add [README.md]  
git commit - "clavesssh"  
git push origin main   



