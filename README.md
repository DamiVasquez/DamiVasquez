/*Damasco Oxcal*/

/*
  
  Fundacion kinal
  Centro Educativo Tecnico Laboral Kinal
  Quinto Perito
  Quinto Electronica
  Codigo Tecnico: EB5AV
  Curso: Taller de electronica digital y reparacion de computadoras I
  Proyecto: Ciclo WHILE
  Dev: Profe. Alejandro Lopez Navas
  Fecha: 04 de abril 
  
  */

    int switch_state = 0;

    void setup() {
      pinMode (3, OUTPUT);
      pinMode (4, OUTPUT);
      pinMode (5, OUTPUT);
      pinMode (2, INPUT);
    }
void loop() {
switch_state = digitalRead(2);

if(switch_state == LOW)
{
digitalWrite(3, HIGH);
digitalWrite(4, LOW);
digitalWrite(5, LOW);
}
  else
  {
    
  digitalWrite(3, LOW);
  digitalWrite(4, LOW);
  digitalWrite(5, HIGH);
  
  delay(250);
  digitalWrite(4, HIGH);
  digitalWrite(5, LOW);
  delay(250);
  }
}
