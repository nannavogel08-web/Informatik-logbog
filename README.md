# Informatik-logbog
En logbog over hvad vi laver i informatik<br>


# Grundforløb:
Vi har arbejdet med: Applab, gestaltlove<br>

Vi har eksperimenteret med applab, og lavet en app der kan udregne skæringspunktet mellem to linære grafer, og hældningen og skæringspunkterne med x-aksen for en 2. grads funktion, ud fra funktionsforskrifter.<br>

App til grafer: https://studio.code.org/projects/applab/54a79519-914f-4cd8-b103-00308e2923bb/edit 

Getsaltlovene: Principper for hvordan en hjemmeside/app skal se ud og fungere for at være brugervenlig


# 1. G

## Programering
Vi har lært om: Variabler, if/else statements, løkker, lister, fysiksimulering<br>
<br>
Vi prøvede os frem med en "bold" der kunne "hoppe" rundt på skærmen <br>
Derefter udviklede vi det til flere bolde, der kunne interagere med hinanden.<br>
<br>
Vi lavede noget kode der lavede 3 punkter og så lavede punkter halvejs mellem punkterne, og så halvejs mellem de punkter osv. hvilket dannede Sierpinski-trekant. Jeg arbejde lidt med at få den til at få forskellige farver. (https://editor.p5js.org/Nanna0817/sketches/HnEshsXFU)<br>
``` Her er noget kode
 var StartX=100 
  var StartY=350 
  var DestX=200
  var DestY=100
  var Xkoordinater=[] 
  var Ykoordinater=[] 

function setup() {
  createCanvas(400, 400);
  background(0);
  strokeWeight(1)
  
  Xkoordinater.push(200)
  Ykoordinater.push(0)
  
  Xkoordinater.push(0);
  Ykoordinater.push(400);
  
  Xkoordinater.push(400);
  Ykoordinater.push(400);
  
  index1=((floor)(random(0, 3)))
  StartX=Xkoordinater[index1]
  StartY=Ykoordinater[index1]
}

function draw() {
  
  index2=((floor)(random(0, 3)))

  
  DestX=Xkoordinater[index2]
  DestY=Ykoordinater[index2]
  
  
  point(StartX, StartY)
  point(DestX, DestY)
  
  StartX=(StartX+DestX)/2
  StartY=(StartY+DestY)/2
  
  stroke(150,StartY, StartX)
  point(StartX, StartY)
  
  
}
```
<br>

## Kryptografi
Vi har lært om: Symetrisk/asymetrisk kryptering, cæsarkode, RSA<br>
<br>
Vi arbejdede kort med kryptografi, hvor vi lavede en kode der kunne kryptere og dekryptere cæsar-kode (https://editor.p5js.org/Nanna0817/sketches/sOhjbX8jL)<br>
```Her er koden:
let message = "HEJ EMILIE";
let nøgle = 7;
//når der senere nævnes cipher, vil den printe noget sagt; den er ikke kode når den har ""
let cipher = "";

let alfabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZÆØÅ ";

//ligesom det, der er lavet hvor der beskrives trin for trin; den regner det bare selv
function caesar_single_character(bogstav, tal) {
  let startIndex = alfabet.indexOf(bogstav);
  let nytIndex = (startIndex + tal) % alfabet.length;
  if (nytIndex < 0) nytIndex += alfabet.length;
  let nytBogstav = alfabet[nytIndex];
  return nytBogstav;
}
function caesar(besked, nummer) {
  //laver alfabetet uendeligt
  nummer = nummer % alfabet.length;
  let resultat = "";
  for (let x of besked) {
    resultat += caesar_single_character(x, nummer);
  }
  return resultat;
}

function setup() {
  console.log(message);
  cipher = caesar(message, nøgle);
  console.log(cipher);

  //message + key = cipher, ergo må message = cipher - key
  let dekrypteret = caesar(cipher, -nøgle);
  console.log(dekrypteret);
}
console.log("KEY:" + nøgle + "->" + (nøgle % alfabet.length));
```
<br>

## 3D
Vi har brugt: Fusion, Cura (Creality CR10S-pro), Bambu studio (Bambu lab P2S)<br>
Vi har arbejdet med 3D design og 3D printning, hvor vi har brugt programmet Fusion til at designe nogle 3D modeller, og derefter printe dem på skolens 3D printere<br>
Her er den figur jeg lavede <img width="1497" height="815" alt="image" src="https://github.com/user-attachments/assets/130c6a33-945e-4fbe-b49f-b5f1b19c785e" />

<br>
