`🇫🇷 Français`&emsp;🇬🇧 [English](routage_EN.md)

# Motorcycle/routing
Des calculs de routage pour 3 types d'utilisation moto, chacun de ces routages calcule un itinéraire en fonction des infos disponibles dans OpenStreetMap.
<br>

voir ici **[pour l'installation](installation.md)**<br>
explications sur les catégories de **[chemins](https://github.com/OsmAnd-Rendering/Motorcycle/wiki/hi%C3%A9rarchie-des-chemins)**

## gros trail 
<b>ne vous fera passer QUE par les chemins faciles (les marrons) et s'il n'en trouve pas, par la route et de tout petits bouts de certains chemins verts.</b>
<br>
- respecte les interdictions (**chemins en rouge** sur la carte)
- respecte les barrières (**points rouges** sur la carte)
- les chemins "**privés**" sont gérés comme avec le profil par défaut d' OsmAnd.
- les chemins "**interdits**" sont regroupés sous le switch "<b>pas d'interdiction</b>" dans "<b>Eviter les routes</b>".
- :bulb: il y-à un autre switch dans "<b>Eviter les routes</b>" pour activer un mode "<b>pas de chemins</b>" qui évite au maximum les chemins en restant sur les routes les plus petites possible.
- :bulb: il y-à un autre switch dans "<b>Eviter les routes</b>" pour activer un mode "<b>si chemins secs</b>" qui rajoute quelques chemins "**verts**" de la carte au cas ou il n'y aurai pas de chemins "**marrons**" à proximité.<br> :warning: Attention à la boue avec des pneus non adaptés !
- considère toutes les routes au même niveau et donc tracera au plus direct.

**:warning: dans les "Paramètres de l'itinéraire" ne cochez pas "utiliser un algorithme de routage A à 2 phase**<br>
<i> sinon vous ne prendrez que de la route</i>

<i>(mettez des points intermédiaires pour "forcer" le détour par les "bons" chemins s'il n'y en à pas en ligne directe).</i>
<br>

## petit trail
<b>vous fera éviter les sentiers et footway mais prendra tous les chemins sauf ceux indiqués "impassable"</b>
<br>
- respecte les interdictions (**chemins en rouge** sur la carte)
- respecte les barrières (**points rouges** sur la carte)
- les chemins "**privés**" sont gérés comme avec le profil par défaut d' OsmAnd.
- les chemins "**interdits**" sont regroupés sous le switch "<b>pas d'interdiction</b>" dans "<b>Eviter les routes</b>".
- privilégie les itinéraires de randonnée et VTT par rapport aux routes.
- considère tous les chemins de la même façon (pas de carrossable ou de boueux) <br>:bulb: <b>SAUF</b> si le switch "<b>trie les chemins</b>" dans "<b>Eviter les routes</b>" est actif (coché) il va hiérarchiser les chemins du plus carrossable à inconnu.
<i><br>
 dans les faits il va pénaliser de plus en plus les chemins qui sont les moins praticables <br>pour aller d'un point A à un point B si 2 chemins à peu près équivalents en distance existent, le moteur de calcul du routage prendra le plus praticable, la proportion de route augmente si les chemins ne sont pas renseignés dans OpenStreetMap.</i>
- considère toutes les routes au même niveau et donc tracera au plus direct.

<i>( ne mettez pas de points trop éloignés pour accélérer le calcul -tous les 100 km par exemple )</i>
 
## enduro
<b>vous fera passer partout sauf escaliers et pistes cyclables et bien sur les points noirs (impassables ^^).</b><br>
- tous les switchs sont inactifs (tout est actif, les gués, les routes gelées, l'accès au privé etc)
- respecte les interdictions "**no**" et "**private**" <b>SAUF</b> si le switch "<b>Pas d'interdit</b>" est actif.
- respecte les barrières absolues (chaine, portail etc)
- priorité inférieure pour les **points rouges** de la carte qui seront évités si alternative.
- considère les footway comme des path (beaucoup de sentiers sont indiqués footway à tort)
- privilégie les itinéraires balisés (rando et VTT)
- privilégie légèrement les sentiers aux chemins.
- toutes les routes sont au même niveau il trace au plus direct.

<i>( ne mettez pas de points trop éloignés pour accélérer le calcul - tous les 100 km par exemple )</i><br>
chez moi un calcul entre 2 points distants d environ 200 km prend 2 minutes.<br>
 
## Calcul
Si vous trouvez le calcul trop lent ou que vous n'arrivez pas à calculer un itinéraire
- aller dans "<b>configurer le profil</b>"
- puis "<b>parametres de guidage</b>"
- "<b>caractéristiques du véhicule</b>"
- "<b>vitesse par defaut</b>"

et baissez la vitesse max vers <b>90</b> (ou moins si besoin)<br>
sachez que plus vous la baissez, plus le calcul est rapide mais plus il empreinte de routes.<br>
(n'interdisez pas les autoroutes ou péages, ils sont déjà désactivés)
 
## Exemples
Quand vous calculerez un itinéraire vous aurez accès à des infos sur votre parcours<br>
proportion route / chemins (et sentiers pour "enduro")<br>
type de chemin avec les couleurs correspondantes à celles de la carte avec le style appliqué.<br>

Ici un exemple dans ma région (sud Ouest) (environ 100 km à vol d'oiseau).<br>

avec le routage "<b>gros trail</b>" sans options actives :<br>

<img src="https://user-images.githubusercontent.com/83398215/184142138-352ff7ef-752a-4350-8592-ecd9433d629a.png" width="400">

avec le routage "<b>gros trail</b>" et le switch "<b>si chemins secs</b> actif :<br>
qui rajoute des chemins "**verts**" moins carrossables dans une faible proportion.<br>
(notez que la proportion de route diminue)

<img src="https://user-images.githubusercontent.com/83398215/184142530-e9a10fd9-30d3-4b41-8bd9-331dbd30c0e4.png" width="400">

Avec le routage "<b>petit_trail</b>" et le switch "<b>trie les chemins</b>" actif:<br>
les résultats sont souvent très proche du "<b>gros_trail</b>" avec "<b>si chemins secs</b>" actif lorsque les chemins sont renseignés dans <b>OpenStreetMap</b>.<br>
(mais le type de chemins "vert" change en étant moins "carrossable")
dans le cas ou la majorité des chemins n'est pas précisée le "tri" des chemins impose plus de route à la place de chemins "difficiles".<br>

<img src="https://user-images.githubusercontent.com/83398215/184142977-1e8ee439-8f1a-4301-ae64-ae093a758a44.png" width="400">

Avec le routage "<b>petit_trail</b>" sans le switch "<b>trie les chemins</b>" actif:<br>
la proportion de routes continue de diminuer, les chemins non renseignés dans OpenStreetMap deviennent plus important, jusqu'à représenter la majorité des chemins selon les régions plus ou moins renseignées dans osm.<br>

<img src="https://user-images.githubusercontent.com/83398215/184143477-ba4297bc-d119-4e53-9cab-4f3fe16f45c4.png" width="400">

le routage "<b>enduro</b>" avec en rouge les sentiers.

<img src="https://user-images.githubusercontent.com/83398215/184144556-839f5010-b098-4bc4-9dfc-0c787869d131.png" width="400">


bon ... n'oubliez pas que c'est perfectible et que dans le meilleur des 
cas ça se base sur les informations ajoutées dans OpenStreetMap qui 
peuvent être obsolètes (chemins détruit récemment) ou basé sur une 
impression subjective de celui qui l'a renseigné (niveau de difficulté 
VTT par exemple).
<br>
<br>
 
plus de détails dans le **[wiki](https://github.com/OsmAnd-Rendering/Motorcycle/wiki/%F0%9F%87%AB%F0%9F%87%B7--Routing)**
