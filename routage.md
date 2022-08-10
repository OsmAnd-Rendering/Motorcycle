`🇫🇷 Français`&emsp;🇬🇧 [English](routage_EN.md)

# Motorcycle/routing
Des calculs de routage pour 3 types d'utilisation moto, chacun de ces routages calcule un itinéraire en fonction des infos disponibles dans OpenStreetMap.
<br>

voir ici **[pour l'installation](installation.md)**

## gros trail 
<b>ne vous fera passer QUE par les chemins faciles (les marrons) et s'il n'en trouve pas, par la route et de tout petits bouts de certains chemins verts.</b>
<br>
- respecte les interdictions (**chemins en rouge** sur la carte)
- respecte les barrières (**points rouges** sur la carte)
- les chemins "**privés**" sont gérés comme avec le profil par défaut d' OsmAnd.
- les chemins "**interdits**" sont regroupés sous le switch "<b>pas d'interdiction</b>" dans "<b>Eviter les routes</b>".
- il y-à un autre switch dans "<b>Eviter les routes</b>" pour activer un mode "<b>si chemins secs</b>" qui rajoute quelques chemins "**verts**" de la carte au cas ou il n'y aurai pas de chemins "**marrons**" à proximité.
- les routes sont hiérarchisées permettant d'avancer plus vite sur de longues distances sans chemins.

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
- considère tous les chemins de la même façon (pas de carrossable ou de boueux) <b>SAUF</b> si le switch "<b>trie les chemins</b>" dans "<b>Eviter les routes</b>" est actif (coché) il va hiérarchiser les chemins du plus carrossable à inconnu.
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

Ici un exemple dans ma région (sud de Toulouse) entre <b>Castelnaudary</b> et <b>Mazamet</b> (environ 60 km à vol d'oiseau à travers "la montagne noire").<br>

avec le routage "<b>gros trail</b>" sans options actives :<br>

<img src="https://1.bp.blogspot.com/-2jO-scaZT8k/YJzinm1gWHI/AAAAAAAAEic/7Qe9Xhfd9mIbINux-c_4Gw7iRT5DH4ugwCLcBGAsYHQ/w296-h640/GT%255B1%255D.jpg" border="0">


avec le routage "<b>gros trail</b>" et le switch "<b>si chemins secs</b> actif :<br>
qui rajoute des chemins "**verts**" moins carrossables dans une faible proportion.<br>

<img src="https://1.bp.blogspot.com/-VDzxurdpIiI/YJzjwUlMM4I/AAAAAAAAEik/uZcepPSb630Fe-n55IIBL5TmeJz4ZSsfACLcBGAsYHQ/w296-h640/GT_sec%255B1%255D.jpg" border="0">

Avec le routage "<b>petit_trail</b>" et le switch "<b>trie les chemins</b>" actif:<br>
les résultats sont souvent très proche du "<b>gros_trail</b>" avec "<b>si chemins secs</b>" actif lorsque les chemins sont renseignés dans <b>OpenStreetMap</b>.<br>

<img src="https://1.bp.blogspot.com/-MBjJMjwtXE8/YJzlMde6u4I/AAAAAAAAEis/U9_bZUoYHwIWkeWYLDMDDUXSGCLE9SBZgCLcBGAsYHQ/w296-h640/PT_tri%255B1%255D.jpg" border="0">

Avec le routage "<b>petit_trail</b>" sans le switch "<b>trie les chemins</b>" actif:<br>
ici très peu de différence, ça dépends de la proportion de chemins renseignés dans <b>OpenStreetMap</b>,<br>
dans le cas ou la majorité des chemins n'est pas précisée le "tri" des chemins impose plus de route à la place de chemins "difficiles".<br>

<img src="https://1.bp.blogspot.com/-4PDQS4TdN0U/YJzl-K4DbjI/AAAAAAAAEi0/tXv0eyXuGEMS93m2lxKqQqMrqMsf9busgCLcBGAsYHQ/w296-h640/PT%255B1%255D.jpg" border="0">

le routage "<b>enduro</b>" avec le respect des interdictions absolues:<br>en rouge les sentiers.<br>

<img src="https://1.bp.blogspot.com/-lPQmsAg-lZY/YJznCWYqokI/AAAAAAAAEi8/EQTPYrifkY4bNCRXaxVm4Ft8vxnBolyvACLcBGAsYHQ/w296-h640/enduro%255B1%255D.jpg" border="0">

le routage "<b>enduro</b>" sans respect des interdictions:<br>
ce qui le fait "raccourcir" la totalité du parcours.<br>

<img src="https://1.bp.blogspot.com/-3r9uNtRCBgo/YJznZdGuWcI/AAAAAAAAEjE/IQIYaEURhRkv0_W50QshOGITjjCx4U6AQCLcBGAsYHQ/w296-h640/enduro_no-interdit%255B1%255D.jpg" border="0">

bon ... n'oubliez pas que c'est perfectible et que dans le meilleur des 
cas ça se base sur les informations ajoutées dans OpenStreetMap qui 
peuvent être obsolètes (chemins détruit récemment) ou basé sur une 
impression subjective de celui qui l'a renseigné (niveau de difficulté 
VTT par exemple).
<br>
<br>
 
plus de détails dans le **[wiki](https://github.com/OsmAnd-Rendering/Motorcycle/wiki/Routing)**
