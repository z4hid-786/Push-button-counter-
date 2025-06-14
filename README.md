// Define the digital pin where the push button is connected
int Pushbutton = 10;

// Variable to keep track of how many times the button has been pressed
int Count = 0;

void setup() {
  // Set the push button pin as input
  pinMode(Pushbutton, INPUT);

  // Start the Serial Monitor with a baud rate of 9600
  Serial.begin(9600);

  // Print a message to the Serial Monitor
  Serial.println("PUSH BUTTON COUNTER");
}

void loop() {
  // Read the current state of the push button (HIGH when pressed)
  int currentbutton = digitalRead(Pushbutton);

  // If the button is pressed
  if (currentbutton == HIGH ) {
    // Increase the count by 1
    Count++;

    // Print the current count to the Serial Monitor
    Serial.print("Count = ");
    Serial.println(Count);

    // Short delay to avoid counting the same press multiple times
    delay(200);
  }
}
