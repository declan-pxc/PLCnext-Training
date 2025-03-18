# PLC300 Expert
This level is preferably done after [PLC200 Advanced](/PLC200%20Advanced). This means we are building on top of the project done previously.

## Project
- Create local and remote control of the target value for OEE. This target value is controlled by AI1 (slider) for local control.
- Show this 'alarm' on the HMI (bonus points for utilising the alarm FBs - you will need to add the PLCnext Controller library.)
- A library needs to be created (it could also be your entire completed project) or a communication FB
- Mapping the PNIO is very similar to how Ethernet/IP can be mapped. Profinet is not usually this difficult for normal networks - this is just a special case to make you think
- You may find that the MODBUS communication needs to be on a cycle time = 10ms. Perhaps you want to put it into a separate task (idle) or speed up the current one? (reference the example project)
- To map the data to buffer - you can use an array as the source. Reference [github.com/declan-pxc/PLCnext-Examples/Data Mapping](github.com/declan-pxc/PLCnext-Examples/Data%20Mapping)
- Reference [github.com/declan-pxc/PLCnext-Examples/Staterkit](github.com/declan-pxc/PLCnext-Examples/Staterkit) for Python and Node-Red
- Datamapping – use BUF_TO_REAL and REAL_TO_BUF function blocks. If you really don’t like that, there are some options in PLCnextBase Library.

#### Bonus Points
- Calculate your neighbours OEE as well using Avail. Perf. and Qual.
- Utilising alarm FBs for target value (and viewing with OPC UA)
- Set neighbours PLC target value with Node Red and/or through PNIO and MODBUS
- Utilise the use of Function Blocks particularly for communication to make it more 'scalable' with additional devices
- Trigger your python code through IEC61131 [PLCnextBase library](https://www.plcnextstore.com/world/app/1397) > LinuxShellCommand)
- Button on HMI to download the CSV directly to computer
