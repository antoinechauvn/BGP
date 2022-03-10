# BGP
>Border Gateway Protocol (BGP) est un protocole d'échange de route externe (un EGP), utilisé notamment sur le réseau Internet. Son objectif principal est d'échanger des informations de routage et d'accessibilité de réseaux (appelés préfixes) entre Autonomous Systems (AS).

>Les connexions entre deux voisins BGP (neighbors ou peers) sont configurées explicitement entre deux routeurs. Ils communiquent alors entre eux via une session TCP sur le port 179 initiée par l'un des deux routeurs. BGP est le seul protocole de routage à utiliser TCP comme protocole de transport. 

>Il existe deux modes de fonctionnement de BGP : Interior BGP (iBGP) et Exterior BGP (eBGP). iBGP est utilisé à l'intérieur d'un Autonomous System alors que eBGP est utilisé entre deux AS.

### Messages du protocole BGP
| Message | Description |
| --- | --- |
| OPEN | Ce message est utilisé dès que la connexion TCP est établie entre les voisins BGP, il permet d'échanger des informations telles que les numéros d'AS respectifs et les router ID de chacun, et de négocier les capacités de chacun des pairs |
| KEEPALIVE | Maintient la session ouverte. Par défaut le message KEEPALIVE est envoyé toutes les 30 secondes, si 3 KEEPALIVE consécutifs sont absents, le routeur est en panne et la session se ferme |
| UPDATE | Ce message permet l'annonce de nouvelles routes ou le retrait de routes. Mise à jour en cas de modification de topologie |
| NOTIFICATION | Message de fin de session BGP à la suite d'une erreur |
| ROUTE-REFRESH | Définie dans la RFC 291819, la capacité de rafraîchissement des routes est négociée dans le message OPEN et permet de demander/réannoncer certains préfixes après une modification de la politique de filtrage |


![image](https://user-images.githubusercontent.com/83721477/157686483-14889e10-23ff-4422-b21e-16dc84956eee.png)
![image](https://user-images.githubusercontent.com/83721477/157686424-c2b8f6dc-4d93-4c97-9dbb-8f1bc16f9ef9.png)
![image](https://user-images.githubusercontent.com/83721477/157686562-7aff2376-b3a5-4392-a671-9ce7cc4af543.png)
![image](https://user-images.githubusercontent.com/83721477/157687092-26f74e9f-f7fc-4615-9ddd-5cf192d97e3f.png)
![image](https://user-images.githubusercontent.com/83721477/157686621-69ea62f0-a437-4498-9ffc-3f9549815e82.png)
![image](https://user-images.githubusercontent.com/83721477/157686637-1cfd298c-8eb0-457b-b236-6ce211ddf301.png)
![image](https://user-images.githubusercontent.com/83721477/157686901-cec996ba-b607-4b7c-9323-4963df3168ff.png)
![image](https://user-images.githubusercontent.com/83721477/157726546-0f5b9097-cb33-451a-9596-e99c65d3b431.png)


![image](https://user-images.githubusercontent.com/83721477/157687202-f44a3d02-6922-4d77-a865-c29e35f92c91.png)

### Choix du plus court chemin BGP
| N° | Attribut | Description |
| --- | --- | --- |
|1| WEIGHT | Le plus grand |
|2| LOCAL_PREF | La plus grande                               |
|3| Local originated | Préférence pour les routes apprise localement|
|4| AS-PATH | Le plus court                                |
|5|  ORIGIN        | IGP < EGP < ?(Incomplète)                    |
|6|    MED         | Routes avec le plus petit MED                |
|7|  eBGP ou iBGP  | Préférence à des routes eBGP plutôt que iBGP |
|8|  NEXT-HOP      | Les routes qui passent par le voisin avec le cout le plus faible |
|9| eBGP Path Age  | Les routes les plus anciennes                |
|10|  Router ID    | Les routes provenant de peer BGP avec un routeur_ID le plus petit sont préférées |
|11| Neighbor ADDR | Utiliser le chemin qui vient du voisin avec l'IP la plus petite |

![image](https://user-images.githubusercontent.com/83721477/155890858-0aa65ffd-9e58-4ea1-aa3b-a370750fe46f.png)

## Vulnérabilités




https://www.youtube.com/watch?v=oHiZobxnO_o

###### © Ecole Nationale Supérieure d'Informatique d'Alger, AFNOG, Wikipedia
