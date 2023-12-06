# CubeEscape
//https://youtu.be/dFMDIQOpmNE<--- video
setScreen("screen4");
playSound("sound://category_music/clear_evidence_loop1.mp3",true);
var rando = randomnum();
var dy1 = 0;
var dy2 = 0;
var dy3 = 0;
var dy4 = 0;
var dy5 = 0;
var dy7 = 0;
var dy8 = 0;
var dy9 = 0;
var dy10 = 0;
var dx11 = 0;
var dy12 = 0;
var dy13 = 0;
var dy14 = 0;
var dy15 = 0;
var dx17 = 0;
var dx18 = 0;
var dy19 = 0;
var dy20 = 0;
var dx21 = 0;
var up = false;
var down = false;
var left = false;
var right = false;
var score = 0;
onEvent("start","click", function(){
  setScreen("screen1");
});
onEvent("Back1","click", function(){
  setScreen("screen4");
});
onEvent("setting","click", function(){
  setScreen("screen5");
});
onEvent("button6","click", function(){
  setProperty("button6", "background-color","green");
  setProperty("button7", "background-color","rgb(53, 59, 81)");
  playSound("sound://category_music/clear_evidence_loop1.mp3",true);

});
onEvent("button7","click", function(){
  setProperty("button7", "background-color","green");
  setProperty("button6", "background-color","rgb(53, 59, 81)");
  stopSound();
});
onEvent("red", "click", function( ) {
  setProperty("block","icon-color","red");
  setText("red","Selected");
  setText("orange"," ");
  setText("yellow"," ");
  setText("green"," ");
  setText("white"," ");
  setText("black"," ");
  setText("purple"," ");
  setText("blue"," ");
  
});
onEvent("orange", "click", function( ) {
  setProperty("block","icon-color","orange");
  setText("orange","Selected");
  setText("red"," ");
  setText("yellow"," ");
  setText("green"," ");
  setText("white"," ");
  setText("black"," ");
  setText("purple"," ");
  setText("blue"," ");

});
onEvent("yellow", "click", function( ) {
  setProperty("block","icon-color","yellow");
  setText("red"," ");
  setText("orange"," ");
  setText("yellow","Selected");
  setText("green"," ");
  setText("white"," ");
  setText("black"," ");
  setText("purple"," ");
  setText("blue"," ");
});
onEvent("green", "click", function( ) {
  setProperty("block","icon-color","green");
  setText("red"," ");
  setText("orange"," ");
  setText("yellow"," ");
  setText("green","Selected");
  setText("white"," ");
  setText("black"," ");
  setText("purple"," ");
  setText("blue"," ");
});
onEvent("blue", "click", function( ) {
  setProperty("block","icon-color","blue");
  setText("red"," ");
  setText("orange"," ");
  setText("yellow"," ");
  setText("green"," ");
  setText("white"," ");
  setText("black"," ");
  setText("purple"," ");
  setText("blue","Selected");
});
onEvent("purple", "click", function( ) {
  setProperty("block","icon-color","purple");
  setText("red"," ");
  setText("orange"," ");
  setText("yellow"," ");
  setText("green"," ");
  setText("white"," ");
  setText("black"," ");
  setText("purple","Selected");
  setText("blue"," ");
});
onEvent("white", "click", function( ) {
  setProperty("block","icon-color","white");
  setText("red"," ");
  setText("orange"," ");
  setText("yellow"," ");
  setText("green"," ");
  setText("white","Selected");
  setText("black"," ");
  setText("purple"," ");
  setText("blue"," ");
});
onEvent("black", "click", function( ) {
  setProperty("block","icon-color","black");
  setText("red"," ");
  setText("orange"," ");
  setText("yellow"," ");
  setText("green"," ");
  setText("white"," ");
  setText("black","Selected");
  setText("purple"," ");
  setText("blue"," ");
});


onEvent("back2","click", function(){
  setScreen("screen4");
});
onEvent("btneasy", "click", function( ) {
  setScreen("screen2");
  dy1+=1;
  dy2-=1;
  dy3+=1;
  dy4-=1;
  dy5+=1;
  dy7-=1;
  dy8+=1;
  dy9-=1;
  dy10+=1;
  dx11-=1;
  dy12+=1;
  dy13-=1;
  dy14+=1;
  dy15-=1;
  dx17+=1;
  dx18-=3;
  dy19+=1;
  dy20-=1;
  dx21+=3;
});
onEvent("btnhard", "click", function( ) {
  setScreen("screen2");
  dy1+=3;
  dy2-=3;
  dy3+=3;
  dy4-=3;
  dy5+=3;
  dy7-=3;
  dy8+=3;
  dy9-=3;
  dy10+=3;
  dx11-=3;
  dy12+=3;
  dy13-=3;
  dy14+=3;
  dy15-=3;
  dx17+=3;
  dx18-=6;
  dy19+=3;
  dy20-=3;
  dx21+=6;
});
function randomnum(){
var random = [];
  for(var i = 0;i<=21;i++){
    var y = randomNumber(1,6);
    appendItem(random,y);
}
  return random;
}
onEvent("random", "click", function( ) {
  setScreen("screen2");
  dy1+=rando[0];
  dy2-=rando[1];
  dy3+=rando[2];
  dy4-=rando[3];
  dy5+=rando[4];
  dy7+=rando[5];
  dy8+=rando[6];
  dy9+=rando[7];
  dy10+=rando[8];
  dx11+=rando[9];
  dy12+=rando[10];
  dy13+=rando[11];
  dy14+=rando[12];
  dy15+=rando[13];
  dx17+=rando[14];
  dx18+=rando[15];
  dy19+=rando[16];
  dy20+=rando[17];
  dx21+=rando[18];
});
timedLoop(25,function(){
moveWalls();
movePerson();
if (overlap("block", "wall1")){
  if(getYPosition("block")<335){
    setProperty("block","y",315);
  }
}
if (overlap("block", "wall3")){
  if(getYPosition("block")<355){
    setProperty("block","y",356);
  }
}
if (overlap("block", "wall5")){
  if(getYPosition("block")<226){
    setProperty("block","y",206);
  }
}
if (overlap("block", "wall2")){
  if(getYPosition("block")<245){
    setProperty("block","y",246);
  }
}
if (overlap("block", "wall6")){
  if(getYPosition("block")<114){
    setProperty("block","y",94);
  }
}
if (overlap("block", "wall4")){
  if(getYPosition("block")<133){
    setProperty("block","y",134);
  }
}
if (overlap("block", "Brick1")||overlap("block", "Brick2")||overlap("block", "Brick3")||overlap("block", "Brick4")
||overlap("block", "Brick5")||overlap("block", "Brick6")||overlap("block", "Brick7")||overlap("block", "Brick8")
||overlap("block", "Brick9")||overlap("block", "Brick10")||overlap("block", "Brick11")||overlap("block", "Brick12")
||overlap("block", "Brick13")||overlap("block", "Brick14")||overlap("block", "Brick15")||overlap("block", "Brick16")
||overlap("block", "Brick17")||overlap("block", "Brick18")||overlap("block", "Brick19")||overlap("block", "Brick20")||overlap("block", "Brick21")){
  score +=1;
  setText("deaths", "Death: " + score);
  setPosition("block",10,390,20,20);
}
checkIfPersonWins();
});
function movePerson(){
if(up == true)
  setProperty("block", "y", getProperty("block", "y") - 4);
if(down == true)
  setProperty("block", "y", getProperty("block", "y") + 4);
if(left == true)
  setProperty("block", "x", getProperty("block", "x") - 4);
if(right == true)
  setProperty("block", "x", getProperty("block", "x") + 4);
if(getProperty("block", "x") <= 0)
  setProperty("block", "x", 0);
if(getProperty("block", "x") + 20 >= 320)
  setProperty("block", "x", 300);
if(getProperty("block", "y") + 20>= 450)
  setProperty("block", "y", 430);
if(getProperty("block", "y") <= 0)
  setProperty("block", "y", 0);
}

function moveWalls(){
  if(getProperty("Brick1", "y") <= 0){
    dy1 = Math.abs(dy1);
  }
  if(getProperty("Brick1", "y") + 20 >= 450)
    dy1 = -dy1;
  if (overlap("Brick1", "wall3"))
    dy1 = -dy1;
  setProperty("Brick1", "y", getProperty("Brick1", "y") + dy1);
  if(getProperty("Brick2", "y") <= 0)
    dy2 = Math.abs(dy2);
  if(getProperty("Brick2", "y") + 20 >= 450)
    dy2 = -dy2;
  if (overlap("Brick2", "wall3"))
    dy2 = -dy2;
  setProperty("Brick2", "y", getProperty("Brick2", "y")  + dy2);
  if(getProperty("Brick3", "y") <= 0)
    dy3 = Math.abs(dy3);
  if(getProperty("Brick3", "y") + 20 >= 450)
    dy3 = -dy3;
  if (overlap("Brick3", "wall3"))
    dy3 = -dy3;
  setProperty("Brick3", "y", getProperty("Brick3", "y") + dy3);
  if(getProperty("Brick4", "y") <= 0)
    dy4 = Math.abs(dy4);
  if(getProperty("Brick4", "y") + 20 >= 450)
    dy4 = -dy4;
  if (overlap("Brick4", "wall3"))
    dy4 = -dy4;
  setProperty("Brick4", "y", getProperty("Brick4", "y") + dy4);
  if(getProperty("Brick7", "y") <= 0)
    dy7 = Math.abs(dy7);
  if(getProperty("Brick7", "y") + 20 >= 450)
    dy7 = -dy7;
  if (overlap("Brick7", "wall1"))
    dy7 = -dy7;
  if(overlap("Brick7","wall2"))
    dy7 = -dy7;
  setProperty("Brick7", "y", getProperty("Brick7", "y") + dy7);
  if(getProperty("Brick8", "y") <= 0)
    dy8 = Math.abs(dy8);
  if(getProperty("Brick8", "y") + 20 >= 450)
    dy8 = -dy8;
  if (overlap("Brick8", "wall1"))
    dy8 = -dy8;
  if(overlap("Brick8","wall2"))
    dy8 = -dy8;
  setProperty("Brick8", "y", getProperty("Brick8", "y") + dy8);
  if(getProperty("Brick9", "y") <= 0)
    dy9 = Math.abs(dy9);
  if(getProperty("Brick9", "y") + 20 >= 450)
    dy9 = -dy9;
  if (overlap("Brick9", "wall1"))
    dy9 = -dy9;
  if(overlap("Brick9","wall2"))
    dy9 = -dy9;
  setProperty("Brick9", "y", getProperty("Brick9", "y") + dy9);
  if(getProperty("Brick10", "y") <= 0)
    dy10 = Math.abs(dy10);
  if(getProperty("Brick10", "y") + 20 >= 450)
    dy10 = -dy10;
  if (overlap("Brick10", "Brick12"))
    dy10 = -dy10;
  if(overlap("Brick10","wall1"))
    dy10 = -dy10;
  setProperty("Brick10", "y", getProperty("Brick10", "y") + dy10);
  if(getProperty("Brick11", "x") <= 0)
    dx11 = Math.abs(dx11);
  if(getProperty("Brick11", "x") + 150 >= 320)
    dx11 = -dx11;
  if(overlap("Brick11","Brick12"))
    dx11 = -dx11;
  setProperty("Brick11", "x", getProperty("Brick11", "x") + dx11);
  if(getProperty("Brick13", "y") <= 0)
    dy13 = Math.abs(dy13);
  if(getProperty("Brick13", "y") + 20 >= 450)
    dy13 = -dy13;
  if (overlap("Brick13", "wall5"))
    dy13 = -dy13;
  if (overlap("Brick13", "wall4"))
    dy13 = -dy13;
  setProperty("Brick13", "y", getProperty("Brick13", "y") + dy13);
  if(getProperty("Brick14", "y") <= 0)
    dy14 = Math.abs(dy14);
  if(getProperty("Brick14", "y") + 20 >= 450)
    dy14 = -dy14;
  if (overlap("Brick14", "wall5"))
    dy14 = -dy14;
  if (overlap("Brick14", "wall4"))
    dy14 = -dy14;
  setProperty("Brick14", "y", getProperty("Brick14", "y") + dy14);
  if(getProperty("Brick15", "y") <= 0)
    dy15 = Math.abs(dy15);
  if(getProperty("Brick15", "y") + 20 >= 450)
    dy15 = -dy15;
  if (overlap("Brick15", "wall5"))
    dy15 = -dy15;
  if (overlap("Brick15", "wall4"))
    dy15 = -dy15;
  setProperty("Brick15", "y", getProperty("Brick15", "y") + dy15);
  if(getProperty("Brick17", "x") <= 0)
    dx17 = Math.abs(dx17);
  if(getProperty("Brick17", "x")+ 20 >= 320)
    dx17 = -dx17;
  if(overlap("Brick17","Brick16"))
    dx17 = -dx17;
  setProperty("Brick17", "x", getProperty("Brick17", "x") + dx17);
  if(getProperty("Brick18", "x") <= 0)
    dx18 = Math.abs(dx18);
  if(getProperty("Brick18", "x") >= 320)
    dx18 = -dx18;
  setProperty("Brick18", "x", getProperty("Brick18", "x") + dx18);
  if(getProperty("Brick21", "x") <= 0)
    dx21 = Math.abs(dx21);
  if(getProperty("Brick21", "x") >= 320)
    dx21 = -dx21;
  setProperty("Brick21", "x", getProperty("Brick21", "x") + dx21);
  if(getProperty("Brick19", "y") <= 0)
    dy19 = Math.abs(dy19);
  if(getProperty("Brick19", "y") + 20 >= 450)
    dy19 = -dy19;
  if (overlap("Brick19", "wall6"))
    dy19 = -dy19;
  setProperty("Brick19", "y", getProperty("Brick19", "y") + dy19);
  if(getProperty("Brick20", "y") <= 0)
    dy20 = Math.abs(dy20);
  if(getProperty("Brick20", "y") + 20 >= 450)
    dy20 = -dy20;
  if (overlap("Brick20", "wall6"))
    dy20 = -dy20;
  setProperty("Brick20", "y", getProperty("Brick20", "y") + dy20);
}
function overlap(id1, id2){
  var x1 = getProperty(id1, "x");
  var x2 = getProperty(id2, "x");
  var y1 = getProperty(id1, "y");
  var y2 = getProperty(id2, "y");
  var width1 = getProperty(id1, "width");
  var width2 = getProperty(id2, "width");
  var height1 = getProperty(id1, "height");
  var height2 = getProperty(id2, "height");
  if (y2 > y1 + height1)
    return false;
  if (y2 + height2 < y1)
    return false;
  if (x2 + width2 < x1)
    return false;
  if (x2 > x1 + width1)
    return false;
  return true;
}

function checkIfPersonWins(){
  if (overlap("block","finish")){
    stopSound();
    playSound("crowd-cheer-ii-6263.mp3", true);
    setScreen('screen3');
    setText("attempts", "You had " + score + " deaths");
  }
}
onEvent("screen2", "keydown", function(e){
  if(e.key == "w")
    up = true;
  if(e.key == "s")
    down = true;
  if(e.key == "a")
    left = true;
  if(e.key == "d")
    right = true;
});

onEvent("screen2", "keyup", function(e){
  if(e.key == "w")
    up = false;
  if(e.key == "s")
    down = false;
  if(e.key == "a")
    left = false;
  if(e.key == "d")
    right = false;
});
