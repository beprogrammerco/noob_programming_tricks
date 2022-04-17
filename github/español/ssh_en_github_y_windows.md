## Bienvenidos a como agregar y configurar la SSH Key en Github y Windows

### *Primero... ¿Qué carajos es SSH Key?* :worried:

#### Definición by google:

SSH Key es un protocolo de seguridad que permite al usuario conectarse con un servidor o difertentes servicios sin necesidad de estar logeado con su usuario y contraseña cada vez que realiza alguna acción en el server. :sleepy:

**¿No tienes ni idea de que significa?**

:rage: **...**

Bueno, esta es mi definición para noobs:

> " Esto es solamente un protocolo más seguro que permite conectar diferentes servicios/ servers. **EJEMPLO => TU CUENTA DE GITHUB** evitando el tipico inicio de sesión y sin exponer tus credenciales, tu solamente necesitas tener tu private ssh key ( Llave privada ) en el lugar que tu quieres registrar ( :neutral_face: Sí, si tu pc por ejemplo ) y compartir la public ssh key ( Llave publica ) al servicio como en este caso tu cuenta de GitHub, y con esta forma github sabe que esa key es tu pc y tu puedes clonar tus respositorios, hacer diferentes acciones sin necesidad de 1000 configuraciones ( Bueno no. Esto no es verdad, las otras formas son muy fáciles también, pero usando la ssh key tu puedes ser más **PRO** :sunglasses: ) "

### Entonces, ¿Cuáles son los pasos por hacer para esta configuración? :confounded:

**Primero, Windows (En este caso Windows 10/11):**

1. Tu necesitas instalar Git en tu computador, https://git-scm.com/.

*esto no es un tutorial de como instalar github :joy: entonces, si tu no sabes, busca en google bro, es fácil*

2. Abre tu Git Bash ( este programa será instalado cuando tu instales git )

3. Configurando Git

    - **Configuración de credenciales globales de Git**
        - git config --global user.name "Your github name"
        - git config --global user.email "yourgithubemail@gmail.com"

**Finalmente a lo que vinimos :sob:**

Debemos configurar tu ssh key en windows ( recuerda en este caso la version 10/11, *Yo no se si en otras versiones será igual xd* )

**1. En tu git bash, ejecuta este comando**
    
    - ssh-keygen

Primero, te preguntará acerca de la locación donde se guardará la ssh. Por defecto, tu carpeta de usuario contendrá una carpeta llamada .ssh. si lo quieres dejar en locación por defecto, Ejecuta la tecla Enter.

*Nota: si tu no tienes una locación especifica solamente presiona enter :cold_sweat:*

Siguiente, se te preguntará si deseas asignar una contraseña para proteger tu private key. Sin una contraseña, cualquier que obtenga tu private key puede hacerse pasar por ti.

*Nota: si tu no quieres escribir una contraseña para esta ssh key, solamente presiona enter*

*Nota 2: Recuerda :joy: si tu escribirás alguna contraseña, cuando tu estas escribiendo eso no será visible pero relax, tu estás escribiendo.*

*Note 3: Mientras es una buena practica establecer una contraseña, es un poco dificil en Windows guardar esa contraseña de manera que no tenga que escribirlo cada vez que ejecuta un comando en Git.*

Ahora tendrás generadas tus public y private key :kissing:


**2. Si tu abres la ubicación donde fueron almacenadas, ( *Recuerda el primer comando, la primera pregunta fue acerca de la locación, como en este ejemplo en /c/Users/youruser/.ssh*)**

- Allí podrás encontrar el id_rsa ( private ssh key ) y id_rsa.pub ( public ssh key )

Ahora la última parte :blush:

**3. Agregar tu SSH key en GitHub**

- abre la public ssh key, id_rsa.pub
    - Por ejemplo usando cat
    > cat /c/youruser/.ssh/id_rsa.pub

- copia toda la información dentro de este archivo

**Finalmente ve a tu perfil en github, abre configuración => SSH o click en este link https://github.com/settings/ssh/new y agrega la información que tu tienes copiada en el archivo de public key** :dizzy_face:

Ahora tu puedes clonar tus repositorios y ejecutar comandos de tu git usando SSH en github.

**Referencias:**

- Gracias the Valentin Despa ( https://vdespa.medium.com/ ) toda la información usada aquí, fue basada en el siguiente articulo de el  https://medium.com/devops-with-valentine/2021-how-to-set-up-your-ssh-key-for-github-on-windows-10-afe6e729a3c0