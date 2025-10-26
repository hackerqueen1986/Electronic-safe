Core components:
1.Arduino Uno: The brain of the project, which runs the code to process the user input and control the lock. 
2.Keypad: A 4x4 or similar keypad used for entering the password. 
3.LCD Display: A 16x02 or similar LCD to show messages like "Enter Code" or "Access Granted". 
4.Servo Motor or Solenoid: The locking mechanism. A servo motor can physically move a bolt, while a solenoid uses an electromagnetic coil to either push or pull a bolt. 
5.Power Source: A battery or DC power supply to power the Arduino and its components. 
How it works:
1.Initialization: When powered on, the system is in a locked state. The LCD displays a prompt like "Enter Code." The secret code is stored either in the Arduino's EEPROM (for persistence through power cycles) or in a secrets tab in cloud-based projects. 
2.Input: The user enters a code using the keypad. 
3.Verification: The Arduino reads the entered code and compares it to the stored password.
4.Lock/Unlock:
If correct: The Arduino activates the servo or solenoid to unlock the safe, often for a set period (e.g., 5 seconds). The LCD will show "Access Granted". 
If incorrect: An "Access Denied" message is shown on the LCD, and the safe remains locked. 
5.Relocking: The safe automatically locks again after the set time has passed, or the user can manually lock it using a specific button. 
