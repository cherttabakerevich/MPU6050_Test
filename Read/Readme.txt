Первый файл это ShowGY521Data.pde он являеться прогграммой написаной на просцесенге которая визуалезирует данные с датчика мпу6050 что бы он работал нормально надо найти вот эту часть кода 

import processing.serial.*;

Serial  myPort;
short   portIndex = 0;-вот в этой части кода поменять не на номер порта а а какой он по счету это смотриться в моем компьюторе в подкл устройства там будет ком порт и написано какой он по счету .
int     lf = 10;       //ASCII linefeed
String  inString;      //String for testing serial communication
int     calibrating;




//  println("in setup");
  String portName = Serial.list()[portIndex];
//  println(Serial.list());
//  println(" Connecting to -> " + Serial.list()[portIndex]);
  myPort = new Serial(this, portName, 38400); В этой части кода надо изменть последнее число на свою скорость .
  myPort.clear();
  myPort.bufferUntil(lf);
} 
