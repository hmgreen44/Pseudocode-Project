## Hand Washing Pseudocode

## Purpose: Successfully clean hands to users best ability by utilizing water, soap, and a towel

# Start

### Variables
 1. User (hands)
 2. Water dispenser 
   <p>2a.'handleC' - Cold water<br>
   2b.'handleH' - Hot Water<br> </p>
  <p>(Allow user to choose water temp and pressure based on value of 'handleC', 'handleH')</p>
  <p>Water would be calculated on a fixed amount starting at 55F and reaching a maximum of 120F <br></p>
  <p>If 'handleC' is set to any value alone water temp equals 55F, else 'handleH' adds increasing temperature and pressure to a maximum of 120F<br></p>
 3. Water pressure value
  <p>(Pressure in a water-solid system will increase about 100 psi for every 1 F increase in temperature)</p>
 4. Water temp value 55 Fahrenheit or 'F' minimum, 120 'F' maximum
 5. Liquid Soap Dispenser (Assume automatic placement of 1ml of soap on hands if detected)
 6. Soap Quantity (Set to a constant value of 1ml)
 7. Towel

### Inputs
1. User
   <p>Initiate water (True) once either 'handleH' or 'handleC' is not set to default value (False) <br>
   Activate 'handleC' and 'handleH' to desired water temp and pressure values <br>
   Place hands under water <br>
   Place hands directly under automatic soap dispenser <br>
   Wash hands using water for at least 20 seconds <br>
   Turn 'handleH' and 'handleC' back to default position (False) <br>
   Dry hands with towel <br></p>
### Outputs
1. Water dispenser
   <p>Main valve 
    Set to (False) constant by default until 'user' input <br>
    Allows flow of water when 'user' sets value of 'handleC' or 'handleH' from (False) to (True) <br>
    Starts function that determines values of 'handleC' and 'handleH' in real time <br>
    dispenses water based on 'user' input for 'handleH' and 'handleC' position <br>
    continues to dispense exact value presented until value is changed <br>
    ceases flow of water when values are set back to default (False)</p>
2. Soap dispenser
   <p>0.7ml is the lowest dose sufficient to comfortably spread across all surfaces of most people's hands <br>
   by default would be set to (False)
    **IMPORTANT** has a sensor to detect if 'user' is requesting soap called "soapSensor"
   checks in real time for 'user' hands under light sensor
   If sensor detects 'user' activate soap dispenser
   dispenses by default 1ml of soap onto users hand
   after soap is dispensed set sensor value back to false for (5) seconds called "soapCooldown"
   after (5) seconds set sensor back to real time check for 'user'
   soap dispenser should return to default value (false) after 1ml has left measuring container
3. Towel
   Absorb water </p>

### Rough Idea of hand washing function/console
<p>init HandWashing <br>
"Water Dispenser" return (False) <br>
"soapSensor" checking for 'user' input <br>
"Soap Dispenser" return (False) <br>
'User' Activate 'handleH' 60% 'handleC' 50%  <br></p>
<p>//If 'handleC' is set to any value alone water temp equals 55F, else 'handleH' adds increasing temperature and pressure to a maximum of 120F</p>
<p>Dispensing 'water' return (True) <br>
"soapSensor" detects 'User' <br>
Dispensing 1ml of soap <br>
Activate "soapCooldown" <br>
5... <br>
4... <br>
3... <br>
2... <br>
1... <br>
"soapSensor" checking for 'user' input <br>
"soapSensor" return false <br>
"Water Dispenser" set to default value return (False)</p>


# END







    



