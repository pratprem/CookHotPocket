CookHotPocket
=============

code for cooking a hotpocket after connecting to an arduino


int led1 = 6; // on
int led2 = 4; // off
int led3 = 8;    

void setup() {                
 
  pinMode(led1, OUTPUT); 
pinMode(led2, OUTPUT);
digitalWrite(led1,HIGH);
digitalWrite(led2,HIGH);

Serial.begin(9600);

}

void loop() {




if(Serial.available())
{
  int hotpocket = Serial.parseInt();
  if(hotpocket==1)
  {
  cookhotpocket();
  }else
  {
    delay(1000);
  }

}  

                
  
}



void cookhotpocket()
{
 for(int i = 0;i<5;i++)
{
  digitalWrite(led1, LOW); 
  delay(100);             
  digitalWrite(led1, HIGH); 
  delay(400);
}  
}
