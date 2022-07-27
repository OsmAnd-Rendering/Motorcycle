# Motorcycle
off road motorcycle render style and routing for OsmAnd Android and iOS

Style focused on off-road motorcycle use with the track classified by "difficulty" linked to the type of machine and the details present in OpenStreetMap.

Routing calculations for 3 types of motorcycle use are under "branch" routing https://github.com/OsmAnd-Rendering/Motorcycle/tree/routing

osf files for automatic install are under "branch" configuration https://github.com/OsmAnd-Rendering/Motorcycle/tree/configuration

more detail here : https://osmtopo.blogspot.com/2021/02/style-pour-osmand.html

## Changements notables par rapport aux styles standard :
<br>
- Chemins identifiés visuellement par carrossabilité (couleurs)<br>
- POI utiles / intéressants mis en évidence<br>
- Difficulté des sentiers à partir des tags VTT et pédestre<br>
- Simplification pour lisibilité des itinéraires VTT/pédestre<br>
- Réglages supplémentaires pour la lisibilité en roulant<br>
<br><br>
---

## Screenshots<br>

| <img src="https://1.bp.blogspot.com/-80KFHZxn-x0/YHhVVHgiDqI/AAAAAAAAEgw/MLuJSVUiiOQsHM9bJUrFQRJCdPtF02YmgCLcBGAsYHQ/s0/millau_cricri_50_1km.jpg" width="250" /> | <img src="https://1.bp.blogspot.com/-cEhzfD_lhDM/YHhTZ3UGs9I/AAAAAAAAEgo/C6xCHkJYfHg21bxSQ9YYdhXif-gmv-v5ACLcBGAsYHQ/s0/millau_cricri_50_2km.jpg" width="250" /> | <img src="https://1.bp.blogspot.com/-exeX47jqhkE/YHl78COV4-I/AAAAAAAAEhQ/I3XvrOUpvmkKBi8QpOHZ5aZRpA1k255AQCLcBGAsYHQ/s0/balisages.jpg" width="250" /> |
| :-------------: | :-------------: | :-------------: |

### 
| <img src="https://1.bp.blogspot.com/-4PDQS4TdN0U/YJzl-K4DbjI/AAAAAAAAEi0/tXv0eyXuGEMS93m2lxKqQqMrqMsf9busgCLcBGAsYHQ/w296-h640/PT%255B1%255D.jpg" width="250" /> | <img src="https://1.bp.blogspot.com/-VDzxurdpIiI/YJzjwUlMM4I/AAAAAAAAEik/uZcepPSb630Fe-n55IIBL5TmeJz4ZSsfACLcBGAsYHQ/w296-h640/GT_sec%255B1%255D.jpg" width="250" /> | <img src="https://1.bp.blogspot.com/-2jO-scaZT8k/YJzinm1gWHI/AAAAAAAAEic/7Qe9Xhfd9mIbINux-c_4Gw7iRT5DH4ugwCLcBGAsYHQ/w296-h640/GT%255B1%255D.jpg" width="250" /> |
| :-------------: | :-------------: | :-------------: |
<br>

---

## Télécharger le rendu
Applicable sur PC, Android et iOS.

- Télécharger le fichier en faisant un clic droit ou appui long sur [ce lien](https://github.com/OsmAnd-Rendering/Motorcycle/blob/main/enduro.render.xml)
    - Télécharger la cible du lien.<br><br>

---

## Légende
### les chemins carrossables considérés comme faciles sont en trait épais marron foncé (pointillé si un peu moins lisse)

 

ils apparaissent en premier à un niveau de zoom éloigné.
ce sont les éléments OpenStreetMap suivants:

"tracktype=grade1"<br>
"tracktype=grade2"<br>
"smoothness=intermediate"<br>
"smoothness=good"<br>
"smoothness=excellent<br>
"surface=paved"<br>
"surface=asphalt"<br>
"surface=concrete"<br>
"surface=concrete:lanes"<br>
"surface=concrete:plates"<br>
"surface=paving_stones"<br>
"surface=sett"<br>
"surface=cobblestone"<br>
"surface=compacted"<br>
"surface=fine_gravel" <br>

 et pour les pointillés<br>
"tracktype=grade3"<br>
"smoothness=bad"<br>
"surface=gravel"<br>
"surface=pebblestone"<br>

### les chemins non empierrés sont en trait vert.

 
ce sont les éléments OpenStreetMap suivants:<br>
"tracktype=grade4"<br>
"smoothness=very_bad"<br>
"surface=unpaved"<br>
"surface=ground"<br>
"surface=dirt"<br>
"surface=earth"<br>
"mtb:scale=0"<br>
"mtb:scale=1"<br>

### les chemins d'exploitation et les chemins non précisés dans OSM sont en trait vert pointillés à un niveau de zoom plus proche.

 
Lorsque l'option "cacher chemin sans info" est désactivée dans le menu "Détails" du style les chemins non renseignés dans OSM restent en trait continu.

ce sont les éléments OpenStreetMap suivants:<br>
"tracktype=grade5"<br>
"smoothness=very_horrible"<br>
"smoothness=horrible"<br>
"surface=grass"<br>
"surface=mud"<br>
"surface=sand"<br>
"mtb:scale=2"<br>
"mtb:scale=3"<br>

### les chemins interdits sont en rouge (gardent leur type défini avant)

ce sont les éléments OpenStreetMap suivants:<br>
"private"<br>
"no"<br>
"forestry"<br>
"agricultural"<br>
"destination"<br>
"customers"<br>

### les sentiers sont en trait fin noir pointillé
auquel se superposent les informations de difficultés VTT et / ou pédestre

 
des points verts pour un sentier facile pour une moto d'enduro légère<br>
"mtb:scale=0"<br>
"mtb:scale:imba=0"<br>

 
des points oranges pour un sentier "technique" pour une moto d'enduro légère<br>
"mtb:scale=1"<br>
"mtb:scale:imba=1"<br>
"sac_scale=hiking"<br>

 
des points rouges pour un sentier difficile pour une moto d'enduro légère (franchissement)<br>
"mtb:scale=2"<br>
"mtb:scale=3"<br>
"mtb:scale:imba=2"<br>
"mtb:scale:imba=3"<br>
"sac_scale=mountain_hiking"<br>

 
des points noirs pour un sentier impassable pour une moto d'enduro légère<br>
"mtb:scale=4<br>
"mtb:scale:imba=4<br>
"mtb:scale=5<br>
"mtb:scale=6<br>
"sac_scale=demanding_mountain_hiking"<br>
"sac_scale=alpine_hiking"<br>
"sac_scale=demanding_alpine_hiking"<br>
"sac_scale=difficult_alpine_hiking"<br>



vous pourrez aussi rencontrer très rarement des traits fins rouge qui apparaissent à un zoom plus élevé que les sentiers, ce sont des sentiers dont la visibilité est notée "aucune" dans OpenStreetMap, le routage "enduro" pourra vous y faire passer mais ... il n'existe probablement pas. 

et enfin une dernière variante des sentiers qui s'affiche en marron clair car vous n'êtes pas censés les emprunter,  ce sont les "footway" pour OSM, des cheminements piéton exclusivement comme les trottoirs en ville mais qui sont souvent à tort identifié comme tel à la place de sentiers génériques en pleine nature.
barrière: une icône selon le type aux zooms proches et un point rouge à zoom éloigné

les balisages désactivables dans le menu du style
icônes selon le type (GR rouge et blanc, tour de pays rouge et jaune, PR jaune) et surlignage des parcours en jaune pour pédestre et mauve pour VTT

les routes
autoroute

profil autoroutier

primaire

secondaire

tertiaire

route / rue

Les rues piétonnes et les places piétonnes sont en vert.
Les voies de service sont en beige.


tunnel

pont

voies ferrées

désaffectée en vert sur laquelle peuvent se superposer les chemins.

tunnel

pont

Quelques éléments remarquables (les autres sont facilement reconnaissables)
les conduites d'eau forcée ou pipeline

terrain militaire (hachures)

zones protégées type Parc National ou Natura 2000

carrière

ligne électrique

ruine

maison isolée

hameau

---

## Installer le rendu
<table>
    <thead>
    <tr>
        <th>Android</th>
        <th>iOS</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td width="50%"><li> À l'aide d'un gestionnaire de fichiers, <code>déplacez le fichier xml téléchargé</code> dans le dossier:<br><code>Android / data / net.osmand.plus / files / rendering</code><br><li>  <code>Fermez l'application</code> Osmand avec le bouton carré d'android<br><li> Ouvrez OsmAnd, puis dans le menu latéral gauche, sélectionnez <code>Paramétrer la carte</code><br<li> Descendez à <code>Style de la carte</code><br> <li> Sélectionnez <code>CycloRoute</code>, votre nouveau rendu.<br><li> Terminé ! 🎉</td>
        <td><li> Ouvrez votre téléchargement, puis choisissez <code>Ouvrir avec OsmAnd</code>. Votre style a été importé!<br><li> Ouvrez OsmAnd, puis dans le menu latéral gauche, sélectionnez sur <code>Paramétrer la carte</code><br><li> Descendez à <code>Style de la carte</code><br><li> Sélectionnez <code>CycloRoute</code>, votre nouveau rendu.<br><li> Terminé ! 🎉</td>
    </tr>
    <tbody>
</table>

<br>

---

