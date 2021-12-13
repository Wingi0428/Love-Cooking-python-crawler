# my_music_game
Imitating a game called world project
PImage img,imgleft,imgup, imgright, imgdown;
import processing.sound.*;
SoundFile sound;
void setup(){
  size(1600,900);
  img = loadImage("BG.png");///載入img
  imgleft = loadImage("left.png");
  imgup = loadImage("up.png");
  imgright = loadImage("right.png");
  imgdown = loadImage("down.png");
  sound = new SoundFile(this, "bensound-anewbeginning.mp3");///載入sound
  sound.play();
}
void draw(){
  image(img, 0, 0, 1600, 900);///BG img
  image(imgleft, 465, 800, 85, 90);
  image(imgup, 665, 800, 85, 90);
  image(imgright, 865, 800, 85, 90);
  image(imgdown, 1065, 800, 85, 90);
  ellipse(mouseX, mouseY,50,50);///mouse
  line(400, 0, 400, 900);///line直
  line(600, 0, 600, 900);///line直
  line(800, 0, 800, 900);///line直
  line(1000, 0, 1000, 900);///line直
  line(1200, 0, 1200, 900);///line直
  line(400, 800, 1200, 800);///line橫
  stroke(255);///line color:白
  strokeWeight(3);///line寬度
  println("mouse: "+ mouseX+ " "+ mouseY);///顯示mouse位置座標
}
