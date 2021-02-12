Hand Washing Pseudocode

//Purpose: Successfully clean hands to users best ability by utilizing water, soap, and a towel

{Variables}
 User (hands)
 Water dispenser 
   'handleC' - Cold water
   'handleH' - Hot Water 
   (Allow user to choose water temp and pressure based on value of 'handleC', 'handleH')
 Water pressure value
  pressure in a water-solid system will increase about 100 psi for every 1 F increase in temperature.
 Water temp value 55 Fahrenheit or 'F' minimum, 120 'F' maximum
 Liquid Soap Dispenser (Assume automatic placement of 1ml of soap on hands if detected)
 Soap Quantity (Set to a constant value of 1ml)
 Towel

{Inputs}
  User
   Initiate water (True) once either 'handleH' or 'handleC' is not set to default value (False)
   Activate 'handleC' and 'handleH' to desired water temp and pressure values
   Place hands under water 
   Place hands directly under automatic soap dispenser
   Wash hands using water for at least 20 seconds
   Turn 'handleH' and 'handleC' back to default position (False)
   Dry hands with towel

{Outputs}
  Water dispenser
   Main valve 
    Set to (False) constant by default until 'user' input
    Allows flow of water when 'user' sets value of 'handleC' or 'handleH' from (False) to (True)
    Starts function that determines values of 'handleC' and 'handleH' in real time
    dispenses water based on 'user' input for 'handleH' and 'handleC' position
    continues to dispense exact value presented until value is changed
    ceases flow of water when values are set back to default (False)
  Soap dispenser
   //0.7ml is the lowest dose sufficient to comfortably spread across all surfaces of most people's hands
   by default would be set to (False)
    *IMPORTANT* has a sensor to detect if 'user' is requesting soap called "soapSensor"
   checks in real time for 'user' hands under light sensor
   If sensor detects 'user' activate soap dispenser
   dispenses by default 1ml of soap onto users hand
   after soap is dispensed set sensor value back to false for (5) seconds called "soapCooldown"
   after (5) seconds set sensor back to real time check for 'user'
   soap dispenser should return to default value (false) after 1ml has left measuring container
  Towel
   Absorb water (Would have no functions)

Rough Idea of hand washing function/console

"Water Dispenser"return (False)
"soapSensor" checking for 'user' input
"Soap Dispenser" return (False)
'User' Activate 'handleH' 60% 'handleC' 50% 
{Water would be calculated on a fixed amount starting at 55F and reaching a maximum of 120F
  //If 'handleC' is set to any value alone water temp equals 55F, else 'handleH' adds increasing temperature and pressure to a maximum of 120F
}
Dispensing 'water' return (True)
"soapSensor" detects 'User'
Dispensing 1ml of soap
Activate "soapCooldown"
5...
4...
3...
2...
1...
"soapSensor" checking for 'user' input
"soapSensor" return false
"Water Dispenser" set to default value return (False)


END







    



