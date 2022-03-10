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

#### Un Interior gateway protocol (IGP) est un protocole de routage utilisé dans les systèmes autonomes. 
![image](https://user-images.githubusercontent.com/83721477/155890858-0aa65ffd-9e58-4ea1-aa3b-a370750fe46f.png)
