# magdPortfolio

f18magd150lab_01_halverson
 This lab was our first lab and it was space themed so i tried to make the death star.
void setup(){

//background   
background(1);
size(650,400);

//Moon

point(700,300);
fill(90);
ellipse(325,150,250,250);


fill(100);
ellipse(290,100,80,80);
strokeWeight(4);
line(450,150,200,150);

strokeWeight(1);
line(250,101,330,101);
line(289,60,289,140);
line(316,70,263,130);
line(263,70,316,130);

ellipse(290,101,35,35);


point(290,101);
//Stars
noStroke();
fill(255);
ellipse(100,100,10,10);
ellipse(300,403,5,5);
ellipse(255,285,8,8);
ellipse(135,250,6,6);
ellipse(555,203,5,5);
ellipse(217,230,8,8);



}


f18magd150lab_02_halverson
 void setup(){

//background   
background(75,175,220);
size(300,300);

}

void draw(){
  
//ballons 
fill(200,135,213);
triangle(70,160,90,160,80,145);
ellipse(80,100,70,90);
fill(255);
noStroke();
ellipse(80,115,10,10);
ellipse(70,75,10,10);
ellipse(90,130,10,10);
ellipse(70,130,10,10);
ellipse(60,110,10,10);
ellipse(100,105,10,10);
ellipse(95,83,10,10);
ellipse(75,93,10,10);

stroke(10);
fill(255, 140, 125);
triangle(190, 115, 200, 125, 180, 125);
ellipse(190, 75, 60, 80);
noFill();
bezier(190,125, 150, 245, 140, 260, 125, 235);

stroke(10);
fill(100,215,175);
ellipse(200,200, 80,100);
triangle(190,260,210,260,200,250);
noFill();
bezier(198, 265 , 200, 225, 210, 270, 173, 300); 
bezier(80, 160, 90, 175, 96, 171, 33, 285); 

}

f18_magd150_lab09_halverson
PImage img;
import processing.sound.*;
import processing.video.*;
Capture video;
SoundFile song;

void setup(){
  size(300, 300);
  
  img = loadImage("mirror.jpg");
  
  video = new Capture(this, 640, 480);
  video.start();
  
  song = new SoundFile(this, "background_noise.mp3");
  
  song.loop();
  

}

void captureEvent(Capture video){
  video.start();
}

void draw(){
  background(0);
  
  image(img, 0, 0, width, height);
  tint(mouseX, 255, mouseY);
  image(video, 97, 42, 115, 115);
}

f18magdlab05_halverson

void update(int x, int y) {
  if ( overCircle(circleX, circleY, circleSize) ) {
    circleOver = true;
    rectOver = false;
  } else if ( overRect(rectX, rectY, rectSize, rectSize) ) {
    rectOver = true;
    circleOver = false;
  } else {
    circleOver = rectOver = false;
  }
}

void mousePressed() {
  if (circleOver) {
   background(96, 232, 228);
  
   fill(18, 160, 61);
   rect(0, 280, 300, 300);
   noStroke();
   fill(247, 247, 70);
   ellipse(40, 50, 50, 50);
   
   fill(255);
   ellipse(200, 60, 60, 40);
   ellipse(220, 60, 40, 40);
   ellipse(240, 60, 50, 40);
   ellipse(200, 60, 40, 50);
   ellipse(220, 40, 40, 40);
  }
  if (rectOver) {
    background(4, 80, 10);
    fill(9, 222, 24);
    text("8374520387452347501475102475102475102", 0, 20);
    text("4638737657392047364926592659600674535", 0, 35);
    text("3485213845129834518923451823451234581", 0, 50);
    text("5468435432484324542435421318430068426", 0, 65);
    text("0000001111101010111100101000101010111", 0, 80);
    text("2347562407569235629375777777723498523", 0, 95);
    text("4358234562039456293406752376555924563", 0, 110);
    text("2562375693475632487562934756239487567", 0, 125);
    text("2456230475620934756203475623047562235", 0, 140);
    text("2348562039458620394856239465656298562", 0, 155);
    text("5623847562834765987243659023465237465", 0, 170);
    text("3475620374652374652376123762345723457", 0, 185);
    text("5723498672349857293845602847302843766", 0, 200);
    text("5692873465234756238974562387456294562", 0, 215);
    text("6593485602835602385702835702837502374", 0, 230);
    text("3942873957234720395702701870275057308", 0, 245);
    text("34652398452938475-2348572934875239845", 0, 305);
    text("2375623856298350238562836519836510357", 0, 260);
    text("1232353407037111109579872308510386115", 0, 275);
    text("29365183650285629856018602111986413865", 0, 290);
  }
}

boolean overRect(int x, int y, int width, int height)  {
  if (mouseX >= x && mouseX <= x+width && 
      mouseY >= y && mouseY <= y+height) {
    return true;
  } else {
    return false;
  }
}

boolean overCircle(int x, int y, int diameter) {
  float disX = x - mouseX;
  float disY = y - mouseY;
  if (sqrt(sq(disX) + sq(disY)) < diameter/2 ) {
    return true;
  } else {
    return false;
  }
}

f18_magd_lab150_halverson
//this scetch will be a motivational poster.

PFont  serif, segoe;// getting the fonts
import processing.pdf.*;// 


void setup(){
  size(500, 430);
  background(40);
  serif = loadFont("Serif.bold-48.vlw");
  segoe = loadFont("SegoePrint-48.vlw");
  
  beginRecord(PDF, "picure.pdf");
}

void draw(){
  textAlign(CENTER, CENTER);
  
  textFont(serif);//Getting the header and mian points
  textSize(45);
  fill(255);
  text("7 RULES OF LIFE", 250, 30);
  textSize(25);
  text("1. LET IT GO", 250, 70);
  text("2. IGNORE THEM", 250, 120);
  text("3. GIVE IT TIME", 250, 170);
  text("4. DON'T COMPARE", 250, 220);
  text("5. STAY CALM", 250, 270);
  text("6. IT'S ON YOU", 250, 320);
  text("7. SMILE", 250, 370);
  
  
  textFont(segoe);//getting the sub points
  textSize(10);
  text("NEVER RUIN A GOOD DAY THINKING ABOUT A BAD YESTERDAY", 250, 90);
  text("DON'T LISTEN TO OTHER PEOPLE, LIVE A LIFE THAT'S EMPOWERING TO YOU", 250, 140);
  text("TIME HEALS EVERYTHING", 250, 190);
  text("THE ONLY PERSON YOU SHOULD TRY TO BEAT IS THE PERSON YOU WERE YESTERDAY", 250, 240);
  text("IT'S OKAY NOT TO HAVE EVERYTHING FIGURED OUT. KNOW THAT IN TIME YOU'LL GET THERE", 250, 290);
  text("ONLY YOU ARE IN CHARGE OF YOUR HAPPINESS", 250, 340);
  text("LIFE IS SHORT, ENJOY IT WHILE YOU HAVE IT", 250, 390);

}

void keyPressed(){// getting the pdf
  if(key == 'p'){
    endRecord();
    exit();
  }
  
}
