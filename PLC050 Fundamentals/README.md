# PLC Level 50 Fundamentals
This course is designed to take half a day not including the project at the end. It is also designed to make use of the Starterkit. 
When you are running through this, I would encourage you to make use of the other PLC resoures around by searching. If you still have issues, send me an email (see profile) with screenshots/files and detailed information. 
I will continue to update the information here but there is a high chance details are missed in the slides which are explained in person.

## Requirements
- [PLCnext Engineer](https://phoenixcontact.net/product/1046008)
- [PLCnext Starterkit](https://phoenixcontact.net/product/1188165)
- PC with Etherent Interface. [IP Address set](https://github.com/declan-pxc/PLCnext-Examples/tree/main/Starterkit#changing-your-ip-address) to 192.168.1.11

## Training
![Welcome](https://github.com/user-attachments/assets/8ff83e69-5702-48d8-964e-15c8cfab8344)
![Contents](https://github.com/user-attachments/assets/1e7005e5-7602-4dc2-a51c-4eb450235786)

### History
![IR1](https://github.com/user-attachments/assets/e5c9562e-c6cc-4b38-9375-1fa068d601b3)
![IR2](https://github.com/user-attachments/assets/51532b0c-23a9-4c0a-b196-78a2dcc520b0)
![IR3](https://github.com/user-attachments/assets/bdec99d8-b56d-4dd8-8784-6b494cd5692f)

### PLCs
![What is Control](https://github.com/user-attachments/assets/f28f01d6-b378-4d6f-9670-10d1e4cbcd75)
![PLC Operation](https://github.com/user-attachments/assets/85e4a279-c51f-420b-98e8-b1c2f9979728)
![Desining a Control project](https://github.com/user-attachments/assets/8910fb0f-167a-440c-890a-4888fb8d469c)

### PLCnext Engineer
![Slide10](https://github.com/user-attachments/assets/19fe7812-8269-40b5-be2c-2c90901cfa85)
![Slide11](https://github.com/user-attachments/assets/0eff7002-b021-42f4-83e6-8b6030274ddd)
![Add IO](https://github.com/user-attachments/assets/7f7933de-ed1b-481b-bf5b-ec367ef304c3)
![Slide13](https://github.com/user-attachments/assets/b42014fe-142d-444b-9ea0-46b1bc6279c2)
### Programming
#### Datatypes
![Datatypes Overview](https://github.com/user-attachments/assets/292ba464-9dc7-46f8-b492-825cc4e47b82)
![Boolean](https://github.com/user-attachments/assets/68bcc322-c959-4d10-8b7e-cf981efc7758)
#### Variables
![Variables](https://github.com/user-attachments/assets/87c8cf2d-c248-4b0b-a784-f5eaaa3fd3b0)
Enter names for the variables and use the Process Data column to select the Input/Output
![Connecting IO to variables](https://github.com/user-attachments/assets/263dd64c-4eab-40c1-922a-cf65c8097608)

#### Application 1
For each of the applications, press on the `+` sign in the Main program to add a new sheet for each. Also recommended to use new outputs for each `Y_` output so they are not overwritten.
![App1](https://github.com/user-attachments/assets/83151a60-6607-40b5-b036-fc70abbff884)
<details>
  <summary> Solution </summary>
  <img src="https://github.com/user-attachments/assets/793e5f1b-dfa5-4359-86ca-0db5de94f54d" />
</details>
![Bitwise Functions](https://github.com/user-attachments/assets/5ff1a420-7c31-40d2-b2e2-e4991c4c4f6d)

#### Application 2
![App2](https://github.com/user-attachments/assets/25f68297-e532-4377-8832-4d6da3423d56)
<details>
  <summary> Solution </summary>
  Also able to use the XOR to simplify your code.
  <img src="https://github.com/user-attachments/assets/ffbcf7b4-ad89-4942-9cf6-49a5df38632c" />
</details>
#### Application 3
Okay, lets get a little more challenging...
![App3](https://github.com/user-attachments/assets/3b1643eb-2c43-47b7-a7fb-e51df390206b)
<details>
  <summary> Solution </summary>
  <img src="github.com/user-attachments/assets/ba8d496a-e64e-414b-bdcc-a83d6252eb0e" />
</details>

### Break
You should have been working for about 60-90mins now, take a :coffee: break.

### IEC 61131-3 Functions
For some of these I have named them Digital, which doesn't turn into a good name later. I would suggest, for the boolean examples, try use the X0, X1 etc. inputs. For the word/real/int examples, create a new sheet and variables with TYPE WORD.  
![Bistable Functions](https://github.com/user-attachments/assets/bbcf1309-225d-4000-ab54-2cebbd86a74a)
![Words Bistable](https://github.com/user-attachments/assets/6d4b71bd-9f42-4996-b57f-d0972470a613)
![Bit Shift](https://github.com/user-attachments/assets/8e1bf62b-196f-4ba8-b03d-81dc34826a22)
![Reals](https://github.com/user-attachments/assets/42b185c6-7f50-4fc0-922f-52e4c1e6f9e4)
<details>
  <summary> Why aren't the values changing? </summary>
  <strong>Great question!</strong> You may have noticed there is a red cross where usually it is a play button on the PLC.
  This has happened because the PLC is dividing by 0. You should have been taken to the place the execption happened and also shown with a green arrow above the DIV block. You can also see this in the messages box > online log. So how do we fix this?
  Two ways,
  1. Go to the divisor definition, and change the INIT column to be something not zero, or better,
  2. Right click on the DIV block and use the EN enable bit to check if it is not zero. This may become more clear further in the information when we look at these logic blocks.
</details>
![INTs](https://github.com/user-attachments/assets/020ed91b-072f-48a8-8d20-b6c38235908c)
![Timers](https://github.com/user-attachments/assets/b4491308-b257-4ad2-81fb-2faededfbced)
![Counters](https://github.com/user-attachments/assets/9fcb9219-cf72-4faf-a222-211d1acdcae8)
![Analog](https://github.com/user-attachments/assets/28a748d6-0dce-41c8-bfbb-a9eec83c77ae)
![Conversions](https://github.com/user-attachments/assets/4107034d-a4bc-45b3-9ad8-418d02a222d2)
<details>
  <summary> More information </summary>
  You can use the conversion tools if you declare an analogue as a WORD but you can also use a REAL instead when declaring to avoid the need of this conversion.
</details>

### Break
We have gone through quite a significant amount more and here is another good time to break. Next we will look at our final Application.

#### Application 4
![App4](https://github.com/user-attachments/assets/49f7c1b5-6181-49dd-8333-3d9a5bb8e5a7)
<details>
  <summary> Solution </summary>
  <img src="github.com/user-attachments/assets/ba8d496a-e64e-414b-bdcc-a83d6252eb0e" />
  <img src="https://github.com/user-attachments/assets/3ba9a427-09e4-42d2-a225-365f8d23c29d" />
  ![Slide41]()
</details>
![Import Library](https://github.com/user-attachments/assets/cb332fa0-f9df-4dcd-96d7-780861da3db5)
For the next step, also double click on HMI Webserver and change the security to None, this will prevent a login window popping up. If you missed it, you can delete the Login page. Otherwise you will get an error. 
If you get this error, you can right click on the page you created and select it as the startup page.
![HMI](https://github.com/user-attachments/assets/da280780-74eb-4463-82c0-d432dfcf8ef2)

### Break
We have gone through the content now, and it has probably taken a bit over half a day. The next step is looking at completing an application on your own.

### Project
![Slide46](https://github.com/user-attachments/assets/f8a35b8b-b03c-4fa9-b337-5613fbe26ec4)

If you are wanting to learn more about PLCnext, consider our [training courses](https://www.phoenixcontact.com/en-au/industries/plcnext-technology/plcnextlab).
