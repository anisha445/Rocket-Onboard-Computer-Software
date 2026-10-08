# Overview
The onboard computer is the brain of a launch vehicle. It runs real-time software that coordinates, monitors, and manages critical onboard functions during flight.

The Onboard software interacts with multiple systems such as navigation, guidance, control, flight sequencing, sensors, and communication interfaces. It receives data from these systems, processes information according to the defined mission requirements, monitor systems health, and provides the required outputs and status informations.

Because this software operates in a real-time and safety critical environments, verification cannot be limited to checking individual software functions. The software needs to be progressively verified from the unit level up to integrated hardware and real time flight like environments.

My work focuses on the software verification and reliability of onboard computer software using multiple levels of testing.

#Verification and Testing Approach

1) Unit Level Testing
   The objective is to verify that each function behaves correctly for different input conditions before it is evaluated as part of the complete system.
   Testing Includes:
   - Normal operating conditions
   - Boundary conditions
   - Invalid inputs
   - Error condtions
   - Failure paths
   - Initialization and reset conditions
   - Expected output verification

   Typical coverage objective includes:
   - Statement Coverage
   - Branch/Decision Coverage
   - MC/DC Covergae
  
The focus at this level is: 
   - Does each software function behave correctly and handle unexpected conditions as intended.
     
2)Integration Level Testing
 Once individual software components have been verified, they are tested together to verify their interfaces and interactions.
 Integrations testing focuses on how different software functions and subsystems communicate and work togetehr.

     






