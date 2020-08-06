# samples-doc_telidtransponders_unix / UNIX DOC sample code for TELID®200 sensor transponders
This sample code is for handling **TELID®200** sensor transponders on devices running UNIX using a Micro-Sensys RFID reader

[Test LINK: SPC communication mode](../doc/communication-modes/spc)
//TODO Add link See "communication-modes/spc"

## Requirements
* Java IDE (For implementing this sample *eclipse IDE* was used)
* Micro-Sensys RFID reader 
* TELID®200 sensor transponders

> For compatible script files, check [Useful Links](#Useful-Links)

## Implementation
This code shows how to use **RFIDFunctions_3000** class to communicate with a TELID®200 sensor transponder. 
Using this class the communication port can be open/closed. Once the communication with RFID reader is established, a Thread can be started to cyclically search for TELID®200 and read current measurement value.

> Class information is available under API documentation. See [Useful Links](#Useful-Links)

## Steps
Import this project into your IDE and check the communication port name for the RFID reader (for example */dev/ttyUSB0*) and fill the name into the *JComboBox*.
Once the name is added to the code, start the debug/run session.

//TODO screenshot!
<!--- ![Screenshot](screenshot/SampleCode_SpcControl_Java.png) --->

 1. Select the device you wish to connect to, and press CONNECT. Once the connect process finishes, the result will be shown in the EditText on the bottom side, and if the device is connected, the START button will be enabled.
 2. Use *START* button to start the read Thread. The library will automatically detect the TELID® type and show the measurements

### Special Hints for Linux
* Device has to be configured in USB VCP mode (ask microsensys for HowTo)
	* To get VCP port name use:	
		> dmesg | grep FTDI
* To be able to communicate with RFID reader, the user must be part of the group "dialout".
	* To add the user to the group use:
		> sudo gpasswd --add [username] dialout

## Useful Links
 - [JAR Library und API documentation](https://www.microsensys.de/downloads/DevSamples/Libraries/UNIX/microsensysRFID%20-%20jar%20library/)
 - [Check what is possible using our iID®DEMOsoft (section SENSORdemo) for PC! Download it using this link](https://www.microsensys.de/downloads/CDContent/Install/iID%c2%ae%20DEMOsoft.zip)

## Contact
* For coding questions or questions about this sample code, you can use [support@microsensys.de](mailto:support@microsensys.de)
* For general questions about the company or our devices, you can contact us using [info@microsensys.de](mailto:info@microsensys.de)

## Authors

* **Victor Garcia** - *Initial work* - [MICS-VGarcia](https://github.com/MICS-VGarcia/)
