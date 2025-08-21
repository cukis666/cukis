```processing
void setup() {
  size(500, 700);
  background(255);
  smooth();
  fill(0);
  textSize(22);

  // Texto arriba
  text("me hice las uñas de los pies x ti...", 40, 40);

  // Pies simplificados
  fill(200);
  rect(80, 70, 40, 100, 10);  // pie izq
  rect(140, 70, 40, 100, 10); // pie der
  // dedos
  fill(0);
  ellipse(90, 65, 15, 15);
  ellipse(110, 65, 15, 15);
  ellipse(150, 65, 15, 15);
  ellipse(170, 65, 15, 15);

  // Texto intermedio
  fill(0);
  text("pq yo quiero tenerte otra vez", 40, 200);

  // Sol con carita
  float cx = 120, cy = 270;
  fill(255, 255, 0);
  stroke(0);
  ellipse(cx, cy, 80, 80);
  // rayos
  fill(255, 165, 0);
  noStroke();
  for (int i = 0; i < 8; i++) {
    float a = TWO_PI/8 * i;
    float x = cx + cos(a) * 60;
    float y = cy + sin(a) * 60;
    pushMatrix();
    translate(x, y);
    rotate(a);
    triangle(-10, 10, 10, 10, 0, -20);
    popMatrix();
  }
  // cara
  fill(0);
  ellipse(cx - 15, cy - 10, 10, 10);
  ellipse(cx + 15, cy - 10, 10, 10);
  stroke(0);
  strokeWeight(3);
  line(cx - 15, cy + 10, cx, cy + 20);
  line(cx, cy + 20, cx + 15, cy + 10);

  // Texto cerca del sol
  fill(0);
  text("y otra vez", 200, 280);

  // Corazón (pareja simplificada)
  drawHeart(120, 400, 40);
  fill(0);
  text("y otra vez", 200, 420);

  // Caras simplificadas
  fill(200);
  ellipse(120, 520, 60, 80); // cara 1
  ellipse(180, 520, 60, 80); // cara 2
  fill(0);
  ellipse(110, 510, 8, 8);
  ellipse(190, 510, 8, 8);
  line(130, 540, 170, 540); // boca en medio
  fill(0);
  text("y otra vez", 200, 550);

  // Texto final
  text("y otra vez...", 180, 640);
}

void drawHeart(float x, float y, float s) {
  fill(0);
  beginShape();
  vertex(x, y);
  bezierVertex(x - s/2, y - s/2, x - s, y + s/3, x, y + s);
  bezierVertex(x + s, y + s/3, x + s/2, y - s/2, x, y);
  endShape(CLOSE);
}
```
  


