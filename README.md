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



# Servicios Básicos Examples

1.1 - Hacer Hash de Password enviado (el hash se guarda en DB)
http://localhost:3000/request_passcode
JSON POST
{
	"pass": "12345678abc"
}

1.2 - Crear Wallet
http://localhost:3000/wallet
JSON POST
{
	"nick_name": "vlopez",
	"pass": "12345678abc",
	"initialBalance":500
}


2.1 - Explorador de Wallet´s en NODO Array de Wallets
http://localhost:3000/wallet_explore
GET Request 

2.2 - Obtiene la Wallet dado el ID
http://localhost:3000/recupera_wallet
JSON POST 
{
	"ide":0
}

3.1 - Transacciones 
http://localhost:3000/transaction_me_to
JSON POST 
{
	"ide":0,
	"recipient":"04d3c0dc2ebc72800018513170bff9935ffbf99c89c3e5742ec73954cd1aebc107a018c1545c95762fbd31f6608fa641650d451773300c0f22635bef9ae4c3767b",
	"amount": 15
}

3.2 - Transacciones en MEMORY POOL
http://localhost:3000/transactions
GET Request

4. - Explorador de Bloques 
http://localhost:3000/blocks
GET Request

# Licencia
Código publicado bajo la licencia MIT .

Derechos de autor 2019-2021 Christian Padilla
Qbit-Services 
