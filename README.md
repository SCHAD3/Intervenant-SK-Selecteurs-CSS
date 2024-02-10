# Intervenant-SK-Selecteurs-CSS
4/01/24
				*********************************************Tips***********************************************
not a name >Nan> reseau social francophone
https://discord.gg/notaname

Paint> redimensionner l'image pour ameliorer la performance, faciliter le chargement de la page.

Tinify > allege le poids de l'image 

awwwards> selection des meilleurs dev

Fonteawesome:
 Mettre code copy unicode dans le content  
 Au lieu de la balise <i>
Ex: e61b pour icone X (ex-twitter)  
 content:"e61b " 
 content:  <i class=fa-brands ....>
 
 youtube-noccokie.com
 Pour ne pas avoir de pub=> ajouter"-" dans l'url
								yout-ube 
resultat: "nocookies" dans l'url

Utilisation de flex:wrap (renvoie d'un item à la ligne quand plus de place) 
=> items multiple de 6 =>les rangées prennent alors une bonne disposition.
Sur vscode: le chiffre à cote d'un fichier met un warning red/ amber (à éviter lors d'une présentation).

>keyboards shortcut sur vscode:
******************************************************Raccourcis**********************************************************************

||       Flexbox                    ||    Padding||       Fonts||        ||Color||        ||Margin||        ||Display||
|d:f  |display: flex                 |p padding           |fs font-size|  |c color        |m margin|        |d:ib display: inline-block   |
|ai:c |align-items: center           |pr padding-right    |ff font-family |c:ra color rgba|mr margin-right  |d:i display: inline          |
|ai:fs|align-items: flex-start       |pl padding-left     |fw font-weight |op opacity     |ml margin-left   |d:n display: none            |
|ai:fe|align-items: flex-end         |pt padding-top      |                               |mt margin-top    |d:b display: block           |
|jc:c |justify-content: center       |pb padding-bottom   |                               |mb margin-bottom |Visibility                   |
|jc:fs|justify-content: flex-start   |                                                                      |v:h visibility: hidden       |
|jc:fe|justify-content: flex-end     |
|jc:sa|justify-content: space-around |
|jc:sb justify-content: space-between|
|fx flex                             |
|fxg flex-grow                       |
|fxsh flex-shrink                    |
|fxw flex-wrap                       |
|fxd flex-direction                  |
|fxd:c flex-direction: column        |
|as:c align-self: center             |
|as:fs align-self: flex-start        |
|as:fe align-self: flex-end          |

||Overflow||               Position||                   Cursor||
|ov:h overflow: hidden    |pos:r position: relative|cur:p cursor: pointer|
|ov:v overflow: visible   |pos:a position: absolute|
|ov:s overflow: scroll    |pos:s position: static  |
|ov:a overflow: auto      |pos:f position: fixed   |
|ovx:h overflow-x: hidden |
|ovx:v overflow-x: visible|
|ovx:s overflow-x: scroll |
|ovx:a overflow-x: auto   |
|ovy:h verflow-y: hidden  |
|ovy:v overflow-y: visible|
|ovy:s overflow-y: scroll |
|ovy:a overflow-y: auto   |

section>(div>img>)*2 : raccourci pour creer x nb de div
alt+Z retour a la ligne 
ctrl+D : pour selectioner une colonne d'element collé 
alt+ fleche haut 
alt maj fleche bas apres >selection copie

			***********************************************FIN...*********************************************

				*************************************Paralax**************************************************

lorem picsum > photo aleatoire  
piscsum:photos (choisir celles avec random!) 
<img src="https://picsum.photos/200/300?random=1">
<img src="https://picsum.photos/200/300?random=2">
coller le random sur html >

Ex:generation 2 photos aleatoires successivement (au click ?)

{code:java}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="style.css">
  <title>Document</title>
</head>
<body>
  <div class="box">
    <img src="https://picsum.photos/300/200?random=1">
  </div>
  <div class="box">
    <img src="https://picsum.photos/300/200?random=2">
  </div>
</body>
</html>
{code}

Ex: 2 bg de couleurs differentes avec utilistation de deux images sur position fixed. 
En modulant(comment?) la position du premier bg BOX de l'image 1, on decouvre la seconde image sur bg 2 en scrollant vers le haut 
(... à revoir avec le code).
Code à integrer 


Ex: Utilisation de l'emplacement disponible avant et apres la page html avec les selecteurs :before et :after
Effet=>  changement de background lorsque la checkbox est coché blue->red 

code à completer et CSS à ajouter 
.test{
h 
w
bg blue 
}
selecteur input 
[type="checkbox"]{
ex: appearence:none }

[type="checkbox"]:checked~.test{
ex: appearence:none}
bg: red 

#au checked changement de couleur 

.test::before 
.test::before   

Ex: Puzzle d'images,
=> Changement des coordonées des points de jointure du puzzle pour chaque pièce contenu dans une box child.
 benettfeely site pour faire des clip- path "couper des chemins":
 
Revoir le code et l'integrer 
{code:java}
 *{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.box{
  height: 100vh;
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
}
.box:nth-child(1){
  background: rgb(0, 255, 13);
}
.box:nth-child(2){
  background: rgb(26, 82, 211);
}
img{
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
} 

{code}

				*******************Differentes façons de centrer *********************************************

diplay:grid 
place item: center;

justify-content:center; => horizontal;
align-items:center; => vertical;

margin: auto> place le container au centre 

transform origin=> change le point d'origine (situé par défaut en haut à gauche soit top, left).
transform translate => ne change pas le point d'origine(qui garde les coordonées 0,0)mais deplace l'element relativement au point d'origine.

a completer en recuperant le code si possible
				***********************************Inspecter *************************************************
styles           :hov > y a une liste exhaustive de ce qui peut etre ecouter en CSS 

lighthouse (outil google)
cocher les categories > analyser> stat sur tout (performance,responsive, accesibilité, etc...)
=> Guide pour correction des pb (à combiner W3C)! 
But obtenir le feu d'artifice!
Ne fonctionne que sur chrome( edge ?)

				*************************Rappel selecteurs CSS************************************************

transform translate: 
changement de la position du curseur 

:before  /      :after
C'est un emplacement disponible avant et apres ce qui est visible sur la page html
 =>il faut nécessairement ajouter un content pour voir qqch 
 content:" "
 
Selecteur input =>
[type="checkbox"]{
ex: appearence:none }

 ~ tild 
 =>permet de selectionner le frère
 Ex:
[type="checkbox"]:checked~.test{
appearence:none
bg: red }

>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
                         05/01/24 (suite selecteurs CSS livecode)
>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
cdn.js > librairie complete > coller le link en haut html
https://swiperjs.com/
https://blog.hubspot.com/website/css-animation-examples
https://scrollmagic.io/
>>>>>>>>>>>>>>>>>>>>>>HTML>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

	<!DOCTYPE html>
	<html lang="en">
	<head>
		<meta charset="UTF-8">
		<meta name="viewport" content="width=device-width, initial-scale=1.0">
		<link rel="stylesheet" href="style.css">
		<title>EXO</title>
	</head>
	
	<body>
	<section>
		<div class="container">
		<div class="box box1">
			<img src="" alt="">
    </div>
    <div class="box box2">
        <img src="" alt="">
    </div>
       <div class="box box3">
		 <img src="" alt="">
	   </div>
	</div>
	</section>
	</body>
	</html>

                >>>>>>>>>>>>>>>>>>>>>>>>>>CSS>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: #111;
}

section { 
    height: 100vh; 
    display: flex;
    justify-content: center;
    align-items: center;
}

.container { 
    position: relative;
    width: 600px;
    height: 400px;
}

.box {
    width: 100%;
    height: 100%;
    position: absolute; => La position est absolute relativement à l'ascendant rencontré le premier contenant la propriété "relative".
							Ici la proximité la plus proche est celle du .container. (à confirmer c ce que j ai cru comprendre).
						=> Ensemble des .box positionnées en haut à gauche du parent ".container"(ici top, left à 0).
    top: 0; 
    left: 0;
    transition: all 0.5s;
}


.box1 {
    background-color: red;
    background-size: cover;
    clip-path: polygon(0 0, 35% 0, 25% 100%, 0% 100%);
}

.box2 {
    background-color: green;
    background-size: cover;
    clip-path: polygon(35% 0, 74% 0, 66% 100%, 25% 100%);
}

.box3 {
    background-color: yellow;
    background-size: cover;
    clip-path: polygon(74% 0, 100% 0, 100% 100%, 66% 100%);
}
                                        ********************HOOVER*************************
On applique un clip-path en fractionnant le container en 3 lamelles (ou pieces de puzzle) réagissant au survol de la souris. 
(.box de couleurs/ img distinctes pour les différencier ci-dessus).

.container:hover .box3 {
    clip-path: polygon(100% 0, 100% 0, 100% 100%, 100% 100%); => Le mouvement de la lamelle jaune est HORIZONTAL.
}

.container:hover .box1 {
    clip-path: polygon(0 0, 0 0, 0 100%, 0 100%);   => Idem pour la rouge (les points de jointures comportent des coordonées inversées).
}

.container:hover .box2 {
    clip-path: polygon(20% 0%, 80% 0%, 100% 0, 0 0);=> variante des coordonées dans .box2 (20% 0%, 80%) 
	                                                   pour un mouvement VERTICAL de la lamelle jaune.
}

.container .box:hover {                =>ici le hoover sur l'ensemble des box est placé posterieurement 
                                        aux lignes de codes specifiques à chaque box
										Afin que le code soit lu dans le bon ordre de priorité,on va du specifique au général.

    clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
}	
	
