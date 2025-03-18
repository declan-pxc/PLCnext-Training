# PLC Level 200 PLCnext Engineer Advanced
In this course, we look further into PLCnext, particularly programming PLCnext Control using PLCnext Engineer. This is designed as a two-day course and can be registered on the [landing page](https://www.phoenixcontact.com/en-au/plcnextlab).
You can also get in touch with your local sales team to organise.

## Project
View the project PDF document and below are some notes. This project is to be complete during the training course. 

#### OEE Calculations
- OEE % = Availability % * Performance % * Quality %
- Availability % = (Planned - Scheduled - Unscheduled) / Planned 
- Performance % = Actual Production / Planned 
- Quality % = (Actual Production - Scrap - Rework) / Actual Production

#### Additional Notes
- To increment and decrement the scrap, you can use the CTU/CTD/CTUD function block. Right click on it in the definition to get help.
- To edit text, you will need to use the HMI object Text Input.
- The analogue value process data goes from 0..10000 - you could either scale for a total of 1440 minutes / day OR convert it to percentage to work out the value.
- For OPC UA - you can use UAexpert to view the data (optional)
- Don't use the first radial gauge. Use the one in the Default folder.
- For the chart, set up Datalogger session with type TSDB and it will be available in the HMI

#### Bonus Functionality
- Save OEE of the last '5' minutes: max min and average.
- Display a 'warning' when the OEE value is < 75%
- Highlight the least performing area of the OEE calc. (Availability, Performance or quality) IF < 85% to show what needs to be improved.
- Make everything as ‘scalable’ as possible (perhaps you have multiple machines that you need to calculate the OEE of) -
  - User-defined data structures
  - Function Blocks for multiple instances
  - HMI Symbols and/or page templates 
