# task3-servo Motor code

## Table of contents

### Table of contents

* [Task Info](#task-info)
* [Task use servo  Motor code](#task-use-servo-Motor-code)

#task info 


This documentation shows the steps of writing servo Motor code.

# use servo Motor code

'#include <Servo.h>'
 
'int servoPin = 9;'
 
'Servo servo;' 
 
'int angle = 0;   // servo position in degrees'
 
'void setup()'
{
'  servo.attach(servoPin);'
}
 
 
'void loop()'
{
' // scan from 0 to 180 degrees'
 ' for(angle = 0; angle < 180; angle++)'  
  {                                  
 ' servo.write(angle);'               
 ' delay(15);'                   
  }
 ' // now scan back from 180 to 0 degrees'
 ' for(angle = 180; angle > 0; angle--) '   
  {                                
    'servo.write(angle);'           
    'delay(15);'     
  }
}
 

'router code'
''The code to steer the servo motor through the handle is easier than the previous code''

''#include <Servo.h>''
 
''int potPin = 0;''  
''int servoPin = 9;''
''Servo servo;''
 
''void setup()''
{
 '' servo.attach(servoPin);''  
}
 
''void loop()''
{
 '' int reading = analogRead(potPin);     // 0 to 1023''
 '' int angle = reading / 6;              // 0 to 180''
  ''servo.write(angle);  
}''










