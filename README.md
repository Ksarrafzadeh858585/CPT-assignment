PImage img;
void setup() {
  size(500,500);
  img = loadImage("Asdf.jpg"); 
  background(img);
  smooth();
}
float circleA = 100;
float circleB = 50;
float speedA = 10;
float speedB = 5;
int score = 0;
int Error = 0;
boolean gamestate = false;

void draw() {
  //start is set to false until the player clicks on the screen
  if(gamestate != true) {
    textSize(30);
    background(img);
    textAlign(CENTER);
    fill(225);
    text("Start Click", width/2 , height/2);
    score = 0;
    Error = 0;
    if(mousePressed) {
    gamestate = true;
