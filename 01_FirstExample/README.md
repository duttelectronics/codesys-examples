# 01_FirstExample

In this first CODESYS example, we are going to create a project, connect to a PLC on the network, download the program to it, and run it.

## REQUIREMENTS:
A PLC5000 with its IP address in the same range as the PC. In this example, the PLC will be configured with the IP address **192.168.1.59**.

---

## STEPS:

### 1. Start Codesys
Launch the CODESYS software on your PC.

### 2. Create a new project
Select the option to start a new project.
![Create New Project](./images/Image_01.png)

### 3. Select the project type
Choose the "Standard project" type and assign a name to it.
![Select Project Type](./images/Image_02.png)

### 4. Select the device and language
Select the device "Montelec-Cortex-Linux" and set the base program language to Ladder Diagram (LD).
![Select Device and Language](./images/Image_03.png)

### 5. Scan the network
Once the project is created, we will scan the network to locate the PLCs. Double-click on "Device".
![Scan Network Device](./images/Image_04.png)

### 6. Scan Network button
In the "Device" window, click on the "Scan Network" button.
![Click Scan Network](./images/Image_05.png)

### 7. Select the PLC
All PLCs available on the network will appear. In our case, select "PLC59".
![Select PLC](./images/Image_06.png)

### 8. Open the main program
We are going to create the base program. Double-click on "PLC_PRG".
![Open PLC Program](./images/Images_07.png)

### 9. Add a block
In the Ladder editor, drag a "Box with EN" from the ToolBox into the first rung.
![Add Box with EN](./images/Image_08.png)

### 10. Create the variable
Double-click on the block's input and create the variable named `counter`.
![Create Counter Variable](./images/Image_09.png)

### 11. Configure the ADD block
Place a `1` at the other input, and assign the `counter` variable to the output again. Change the block type to `ADD` and set the contact before the block to `TRUE`.
![Configure ADD Block](./images/Image_10.png)

### 12. Download to PLC
Download/send the program to the PLC.
![Download Program](./images/Image_11.png)

### 13. Run the project
Once the project is downloaded, switch the PLC to RUN mode.
![Set to RUN](./images/Image_12.png)

### 14. Verify execution
Once the PLC is in RUN mode, "RUN" will be displayed on the screen, and you will see the `counter` variable incrementing.
![Verify Execution](./images/Image_13.png)

---

> 💡 **Note:** If the program does not enter RUN mode, check that the physical switch on the front panel of the PLC is set to RUN.