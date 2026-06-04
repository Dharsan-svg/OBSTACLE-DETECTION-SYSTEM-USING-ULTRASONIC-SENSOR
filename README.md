

## Circuit Diagram:
<img width="1512" height="920" alt="image" src="https://github.com/user-attachments/assets/13a6780a-136a-42f8-9cd3-7d5c9014c05c" />


## Procedure: //Modify the procedure based on your circuit
## Procedure: 

Step 1: Set Up the Tinkercad Environment
1.	Log in to Tinkercad: Open Tinkercad in your web browser and log into your account.
@@ -53,14 +55,38 @@ Step 7: Save Your Work


## Code:

```
#define echoPin 2
#define trigPin 3
long duration;
int distance;
void setup()
{
  pinMode(trigPin, OUTPUT);
  pinMode(echoPin, INPUT);
  Serial.begin(9600);
}
void loop()
{
  digitalWrite(trigPin, LOW);
  delayMicroseconds(2);
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(10);
  digitalWrite(trigPin, LOW);
  duration = pulseIn(echoPin, HIGH);
  distance = duration * 0.034 / 2;
  Serial.print("Distance: ");
  Serial.print(distance);
  Serial.println(" cm");
}
```

## Output:
 

 <img width="1919" height="1116" alt="image" src="https://github.com/user-attachments/assets/a395feaf-e266-4691-9754-f3928e609f3a" />


## Result

## Result

Result:
The simulation successfully measured the distance between the ultrasonic sensor  HC-SR04 and the object. The real-time distance values were accurately displayed on the serial monitor in centimeters.
