//I2C SDA pin - Arduino A4, SCL pin - A5

#include <DS3231.h>
#include <SoftwareSerial.h>

DS3231  rtc(SDA, SCL); // Init the DS3231 using the hardware interface
SoftwareSerial VFD(6,7); // RX, TX
String(day) = "SUNDAY"; // Init var for clear screen every day
void setup()
{
 
//  Serial.begin(115200); // Setup Serial connection for debugging
   
  rtc.begin(); // Initialize the rtc object
  
  // The following lines can be uncommented to set the date and time
  //rtc.setDOW(WEDNESDAY);     // Set Day-of-Week to SUNDAY
  //rtc.setTime(12, 0, 0);     // Set the time to 12:00:00 (24hr format)
  //rtc.setDate(1, 1, 2014);   // Set the date to January 1st, 2014

 VFD.begin(9600);
 VFD.print("\033[7m"); // clear screen
 VFD.print("\033[2J");
}

void loop()
{
  // Send time
  VFD.print("\033[1;1H"); // set cursor position
  VFD.print(rtc.getTimeStr()); // send to VFD
  Serial.println(rtc.getTimeStr()); // send to serial
  
  // Send Day-of-Week
  VFD.print("\033[2;1H");
  VFD.print(rtc.getDOWStr());
//  Serial.print(rtc.getDOWStr());
//  Serial.print(" ");
  
  // Send date
  VFD.print("\033[2;11H");
  VFD.print(rtc.getDateStr());
//  Serial.print(rtc.getDateStr());
//  Serial.print(" -- ");

  // Send current temperature
  VFD.print("\033[1;15H");
  VFD.print("\164");
  VFD.print("\033[1;16H");
  VFD.print(rtc.getTemp());
//  Serial.print("Temperature: ");
//  Serial.print(rtc.getTemp());
//  Serial.println(" C");

  //clear screen every day
  if (day.compareTo(rtc.getDOWStr()) == 0){ // compare days
//    Serial.println("Day OK"); // debugging sending
    delay (1000); // Wait one second before repeating :)
  }
  else{
    VFD.print("\033[7m"); // clear screen
    VFD.print("\033[2J");
//    Serial.println("Day NOT OK"); // debugging sending
    day = rtc.getDOWStr(); // change day
    delay (1000);
  }

}
