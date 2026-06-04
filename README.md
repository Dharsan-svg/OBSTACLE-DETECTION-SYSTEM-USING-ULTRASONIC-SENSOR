OBSTACLE-DETECTION-SYSTEM-USING-ULTRASONIC-SENSOR

Aim:
To design and simulate a distance measurement system using an ultrasonic sensor HC-SR04 interfaced with an Arduino Uno board in Tinkercad.

Hardware / Software Tools required:

Arduino Uno R3
HC-SR04 Ultrasonic Distance Sensor
Jumper Wires
USB Cable (for simulation purpose in Tinkercad)

Theory:
The ultrasonic distance sensor (HC-SR04) is a widely used electronic component for non-contact distance measurement. It operates on the principle of echo-ranging, where it emits an ultrasonic pulse and listens for its reflection from an object. The time taken for the echo to return is directly proportional to the distance of the object from the sensor. This sensor has two main pins—Trigger and Echo. The Trigger pin is used to send a short pulse (usually 10 microseconds), and the Echo pin receives the reflected signal. The Arduino microcontroller calculates the time interval between sending and receiving the ultrasonic pulse and converts it into distance using a specific formula. The speed of sound in air is approximately 343 meters per second (or 0.034 cm per microsecond). Since the sound travels to the object and back, the measured time is divided by 2. The formula used is: distance = (duration × 0.034) / 2. The sensor is highly suitable for robotics, object detection, and security systems where accurate distance measurement is crucial. The Arduino Uno serves as the brain of this project and controls the sensor, processes the pulse duration, and outputs the result via the serial monitor. Tinkercad provides a simulation environment where this circuit can be virtually built, connected, and tested. Through this setup, users can analyze how the sensor interacts with different distances, and visualize its output in real-time without requiring physical components. This setup not only helps in understanding sensor interfacing but also enhances coding skills through implementation in the Arduino IDE. It is an ideal beginner project for learning microcontroller and sensor interfacing.

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
