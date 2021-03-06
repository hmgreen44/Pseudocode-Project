## Hand Washing Pseudocode

## Purpose: Successfully clean hands to users best ability by utilizing water, soap, and a towel

# Start

### Variables <p>
 1. User (Hands) <br>
 2. Water dispenser HandleC - Cold water, HandleH - Hot Water <br>
- If HandleC is set to any value alone water temp equals 55F, else HandleH adds increasing temperature and pressure to a maximum of 120F<br>
 3. Water pressure value <br>
- Pressure in a water-solid system will increase about 100 psi for every 1 Fahrenheit increase in temperature) <br>
 4. Water temp value 55 Fahrenheit or 'F' minimum, 120 'F' maximum <br>
 5. Liquid Soap Dispenser (Assume automatic placement of 1ml of soap on hands if detected)<br>
- Soap dispenser has a sensor to detect if 'user' is requesting soap called "soapSensor"<br>
 6. Soap Quantity (Set to a constant value of 1ml) <br>
 7. Towel <br>
- Allow user to choose water temp and pressure based on value of HandleC, and HandleH)<br>
- Water temperature would be calculated on a fixed amount starting at 55F and reaching a maximum of 120F</p>

### Inputs
1. User <p>
Initiate water (True) once either HandleH or HandleC is not set to default value (False)
   - Activate HandleC and HandleH to desired water temp and pressure values <br>
   - Place hands under water <br>
   - Place hands directly under automatic soap dispenser <br>
   - Wash hands using water for at least 20 seconds <br>
   - Turn HandleH and HandleC back to default position (False) <br>
   - Dry hands with towel <br></p>
### Outputs
1. Water dispenser <p>
Main valve 
    - Set to (False) constant by default until user input <br>
    - Allows flow of water when 'user' sets value of 'handleC' or 'handleH' from (False) to (True) <br>
    - Starts function that determines values of 'handleC' and 'handleH' in real time <br>
    - Dispenses water based on 'user' input for 'handleH' and 'handleC' position <br>
    - Continues to dispense exact value presented until value is changed <br>
    - Ceases flow of water when values are set back to default (False)</p>
2. Soap dispenser <p>
0.7ml is the lowest dose sufficient to comfortably spread across all surfaces of most people's hands <br>
   - By default would be set to (False) <br>
   - Checks in real time for 'user' hands under light sensor <br>
   - If sensor detects 'user' activate soap dispenser <br>
   - Dispenses by default 1ml of soap onto users hand <br>
   - After soap is dispensed set sensor value back to false for (5) seconds called "soapCooldown" <br>
   - After (5) seconds set sensor back to real time check for 'user' <br>
   - Soap dispenser should return to default value (false) after 1ml has left measuring container <br>
3. Towel
   - Absorb water </p>

### Rough Idea of hand washing function/console
<p>Init HandWashing <br>
"Water Dispenser" return (False) <br>
"soapSensor" checking for 'user' input <br>
"Soap Dispenser" return (False) <br>
'User' Activate HandleH 60% HandleC 50%  <br>
Dispensing water return (True) <br>
"soapSensor" detects 'User' <br>
Dispensing 1ml of soap <br>
Activate "soapCooldown" <br>
"soapSensor" checking for 'user' input <br>
"soapSensor" return false <br>
"Water Dispenser" set to default value return (False)</p>


# END







    



