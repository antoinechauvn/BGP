# BGP
>Border Gateway Protocol (BGP) est un protocole d'échange de route externe (un EGP), utilisé notamment sur le réseau Internet. Son objectif principal est d'échanger des informations de routage et d'accessibilité de réseaux (appelés préfixes) entre Autonomous Systems (AS).

>Les connexions entre deux voisins BGP (neighbors ou peers) sont configurées explicitement entre deux routeurs. Ils communiquent alors entre eux via une session TCP sur le port 179 initiée par l'un des deux routeurs. BGP est le seul protocole de routage à utiliser TCP comme protocole de transport. 

>Il existe deux modes de fonctionnement de BGP : Interior BGP (iBGP) et Exterior BGP (eBGP). iBGP est utilisé à l'intérieur d'un Autonomous System alors que eBGP est utilisé entre deux AS.

### Messages du protocole BGP
| Message | Description |
| --- | --- |
| OPEN | Ce message est utilisé dès que la connexion TCP est établie entre les voisins BGP, il permet d'échanger des informations telles que les numéros d'AS respectifs et les router ID de chacun, et de négocier les capacités de chacun des pairs |
| KEEPALIVE | Maintient la session ouverte. Par défaut le message KEEPALIVE est envoyé toutes les 30 secondes, et un délai de 90 secondes sans message UPDATE ni KEEPALIVE reçu entraîne la fermeture de la session |
| UPDATE | Ce message permet l'annonce de nouvelles routes ou le retrait de routes |
| NOTIFICATION | Message de fin de session BGP à la suite d'une erreur |
| ROUTE-REFRESH | Définie dans la RFC 291819, la capacité de rafraîchissement des routes est négociée dans le message OPEN et permet de demander/réannoncer certains préfixes après une modification de la politique de filtrage |

#### Un Interior gateway protocol (IGP) est un protocole de routage utilisé dans les systèmes autonomes. 
![image](https://user-images.githubusercontent.com/83721477/155891595-fc7f7ae7-a8f4-444a-b608-c6505910288e.png)

![image](https://user-images.githubusercontent.com/83721477/155890654-4eb5e67e-eb3c-4935-bbf9-e8b3c220cd01.png)
![image](https://user-images.githubusercontent.com/83721477/155890672-475525ee-2112-4643-bfe7-b302e4dd6379.png)
![image](https://user-images.githubusercontent.com/83721477/155890681-c1c4d7e5-99ba-469b-a44d-eb6f3e4208a1.png)
![image](https://user-images.githubusercontent.com/83721477/155890684-d5394952-e373-4106-9ea6-2abcca69fa90.png)
![image](https://user-images.githubusercontent.com/83721477/155890693-4848be3e-1f44-4b9b-aae6-fbccf215965e.png)
![image](https://user-images.githubusercontent.com/83721477/155890704-98774475-1357-4968-9fb4-263ed04129e4.png)
![image](https://user-images.githubusercontent.com/83721477/155890761-be6a2dc9-8749-4e68-9b8f-9b1415e809f7.png)
![image](https://user-images.githubusercontent.com/83721477/155890766-b160ed6c-61f2-47c9-b1c5-1e8c3d33ec3f.png)
![image](https://user-images.githubusercontent.com/83721477/155890768-ddb36005-e76e-47eb-b83b-c95458cb0929.png)
![image](https://user-images.githubusercontent.com/83721477/155890772-8b7c4dc6-fdd9-430d-b529-9eb10d7fecb6.png)
![image](https://user-images.githubusercontent.com/83721477/155890779-1b911442-5fd1-4cbf-bcb1-1d52cbe3a12a.png)
![image](https://user-images.githubusercontent.com/83721477/155890786-68bb398b-a8d7-4197-b1a5-efa3ec136af4.png)
![image](https://user-images.githubusercontent.com/83721477/155890792-976861a2-111d-4caf-89b4-56c5e43d3bfa.png)
![image](https://user-images.githubusercontent.com/83721477/155890799-f59664f8-c41c-410c-9588-ca49e4f08bef.png)
![image](https://user-images.githubusercontent.com/83721477/155890801-a1e497c7-5c59-4ac9-b37d-85b0cb92ad7a.png)
![image](https://user-images.githubusercontent.com/83721477/155890808-ab6b2b47-93ae-4c1a-8d08-e041e9047de0.png)
![image](https://user-images.githubusercontent.com/83721477/155890813-2fee84c5-5d74-4cbe-89a0-be679efb1e78.png)
![image](https://user-images.githubusercontent.com/83721477/155890819-c103b0a1-0734-4fd7-83fd-c2cb39c315bb.png)
![image](https://user-images.githubusercontent.com/83721477/155890823-c6a0723a-4eda-4d16-918a-2b4a10800262.png)
![image](https://user-images.githubusercontent.com/83721477/155890827-6512cd10-b21a-4c5b-80c5-2ccb2d5976c3.png)
![image](https://user-images.githubusercontent.com/83721477/155890832-16f23530-c611-4504-84e8-56ec13efee61.png)
![image](https://user-images.githubusercontent.com/83721477/155890847-65f37b13-8499-473f-9974-9f047d1a5ab9.png)
![image](https://user-images.githubusercontent.com/83721477/155890856-041a5dba-8580-4106-bfd9-226d0d5d8f8d.png)
![image](https://user-images.githubusercontent.com/83721477/155890858-0aa65ffd-9e58-4ea1-aa3b-a370750fe46f.png)
