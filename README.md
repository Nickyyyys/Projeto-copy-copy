# Projeto-copy-copy
Reprodução do jogo copy copy 
// variaveis da boliha
let xBolinha = 300;
let yBolinha = 200;
let diametro = 20;
let raio = diametro/2;


let velocidadeX = 6;
let velocidadeY = 4;

// variáveis da raquete
let larguraRaquete = 10;
let alturaRaquete = 60;

function setup() {
  createCanvas(600,400);
}

function draw() {
  background('#081147');
  desenhaBolinha();
  movimentaBolinha();
  verificaBorda();
  desenhaRaquete(0, 170);
}

function desenhaBolinha(){
  
  
  circle(xBolinha,yBolinha,diametro)
}
  
  function movimentaBolinha(){
    
    xBolinha += velocidadeX;
    yBolinha += velocidadeY;
  }
function verificaBorda(){
   if(xBolinha + raio > width || xBolinha - raio < 0){
     velocidadeX *= -1;
   }
  if(yBolinha + raio > height || yBolinha - raio < 0){
     velocidadeY *= -1;
   }
}

function desenhaRaquete(x,y){
  rect(x,y, larguraRaquete, alturaRaquete);
}
