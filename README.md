
int startX = 0;
int startY = 150;
int endX = 0;
int endY = 150;
int diameter = 10;
void setup()
{
  size(300,300);
  strokeWeight((float)Math.random()*3);
  background(1);
  noFill();
  frameRate(10);
}
void draw()
{
  fill(0,0,0,15);
  rect(0,0,300,300);
  ellipse(150, 150, diameter, diameter);
  diameter = diameter + 20;
  if(diameter > 400)
    {
      diameter = 10;
    }
  stroke((int) (Math.random()*256), (int) (Math.random()*256), (int) (Math.random()*256));
  while(endX < 300)
    {
      endX = startX + (int)(Math.random()*8);
      endY = startY + (int)(Math.random()*17)-2;
      line(startX, startY, endX, endY);
      startX = endX;
      startY = endY;
    }
}
void mousePressed()
{
  startX = 0;
  startY = 0;
  endX = 20;
  endY = 50;

}
