/* Prosthetic Arm  v1.1
 * Covarrubias, Juliana
 * Martinez, Gisela 
 * Navarro, Revanna
 * Sun, Jason
 * Purpose: Open and Close Fingers with a Switch
 */

#include <Servo.h>
int button1 = 4; //button pin, connect to ground to move servo
int press1 = 0;
Servo servo1;

void setup()
{
  pinMode(button1, INPUT);
  servo1.attach(7);
  digitalWrite(4, HIGH); //enable pull ups to make pin high
}

void loop()
{
  press1 = digitalRead(button1);
  if (press1 == LOW)
  {
	servo1.write(50);
  }
  else {
	servo1.write(0);
  }
}
