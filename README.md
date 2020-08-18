# Nodo-Maestro-Criptomoneda
Repositorio para levantar un nodo Maestro de Criptomonedas con servicios de blockchain , wallet, transacciones y minado-.

En el presente se proporciona la información para el uso de cadena de bloques.

Un Nodo para crear aplicaciones y servicios con Node JS, es extensible y configurable para adaptarse de manera agil a plataformas de gestión y administración.
El Nodo contiene servicios de blockchain, servicios de wallet y transaferencias de criptomonedas, minado de transacciones.
El nodo permite extender sus capacidades lo que lo hace escalable de acuerdo a sus necesidades.
Es posible agregar un backoffice y exponer API services para su comunidad.


# PreRequisitos

Systema Windows 10
2 RAM Core i3 (Minimo)
Open PORT Configuration 

- Install Git
- Install Composer
- Install Node JS
- Install Babel 
- Install NodeMon

Otorgar PERMISOS Full a Carpeta del Nodo


# Uso Como Servidor Independiente 

- Clonar de https://github.com/ChrisQbit/Nodo-Maestro-Criptomoneda.git
- npm install
- Composer Install

Si tenemos problemas con los comandos en CMD de Windows 
npm install --save-dev cross-env
2.2 - En el package json poner cross-env antes del HTTP_PORT

Una vez con todo componente instalado en el servidor accedemos via CMD (Command Line) a la ruta de nuestro nodo
example:
C:/ruta_al_nodo/MASTER_NODO/





# RUNNING NODE / CORRIENDO NODO MAESTRO
Para que el nodo comience a trabajar, Corremos el comando creado via YARN
/MASTER_NODO>yarn start

*****La consola mostrara lo siguiente y el NODO ESTA LISTO y en funcionamiento en el Puerto:3000
Service HTTP:3000 listening...
Service ws:5000 listening...
[ws:socket] connected.





# ABRIR WEBSOCKET / OPEN WEBSOCKET
Es posible agrehar websocket para conexion entre puntos de nodos, para abrir un websocket acceda a la consola a la ruta del NODO y ejecute el comando:
/MASTER_NODO>yarn start:2  


***$ cross-env HTTP_PORT=3001 P2P_PORT=5001 PEERS=ws:localhost:5000 babel-node ./service/index
Service HTTP:3001 listening...
Service ws:5001 listening...
[ws:socket] connected.


Tome en cuenta que el host el donde se aloja el NODO, de ser el caso sustituya localhost por su dominio real.
http://localhost:3000/





# Licencia
Código publicado bajo la licencia MIT .

Derechos de autor 2019-2021 Christian Padilla
Qbit-Services 
