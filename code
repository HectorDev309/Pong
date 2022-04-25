let xBola = 600
let yBola = 300
let xBarra = 30
let yBarra = 300
let xBarra2 = 1165
let yBarra2 = 300
let controle = 1

let diametro = 50
let raio = diametro / 2
let pontos1 = 0
let pontos2 = 0

let velocidadeX = 9
let velocidadeY = 8

let ponto
let bater
let musica

function preload(){
  ponto = loadSound('ponto.mp3');
  bater = loadSound('raquetada.mp3');
 
}
function setup() {
  createCanvas(1200, 600);
 
}

function draw() {
  //sprites
  background(0);
  rect(xBarra, yBarra, 10, 150)
  rect(xBarra2, yBarra2 - 75, 10, 150)
  rect (600, 0, 3, 600)
  circle(xBola, yBola, 50);
  
  //movimento da bola
  xBola += velocidadeX;
  yBola += velocidadeY;
  
  //pontuação
  textAlign (CENTER)
  textSize (50)
  fill (255, 255, 255);
  text (pontos1, 545, 10, 20, 95 )
  text (pontos2, 645, 10, 20, 95 )
  
  //movimento da raquete inimiga
  if (xBola > 1070 && xBola < 1080){
    yBarra2 = yBola + random(-50, 50)
  }
  
  //colisão da bola
  if (xBola - raio < xBarra + 10 && xBola - raio > xBarra && yBola > yBarra && yBola < yBarra + 150) {
    bater.play()
    velocidadeX *= -1
  }
  if (xBola + raio > xBarra2 && xBola + raio < xBarra2 + 10 && yBola > yBarra2 - 75 && yBola < yBarra2 + 75){ 
    bater.play()
    velocidadeX *= -1
  }
  if (xBola > width)  {
    ponto.play()
    pontos1 += 1;
    xBola = 600
    yBola = 300 }
  
  if (xBola < 0)  {
    ponto.play()
    pontos2 += 1;
    xBola = 600
    yBola = 300}
  
  if (yBola + raio > height || yBola - raio <0) {
    velocidadeY *= -1;
  }
   
  //controle
  if (controle === 1){
    yBarra = mouseY - 75
  }
  if (controle === 0){
    if (yBarra > 0 || yBarra + 75 < height){
      if (keyIsDown(UP_ARROW)) {
    yBarra += -10
    }
      if (keyIsDown(DOWN_ARROW)) {
    yBarra += 10
    }}}}
