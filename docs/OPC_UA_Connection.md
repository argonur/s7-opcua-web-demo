# Configuration of OPC UA Server in TIA Portal
1. Open your TIA Portal and upload your program to a PLC 1500.

2. Go to Device Configuration.

3. In the PLC properties, find the OPC UA option (located next to Protection & Security).

4. In OPC UA, find the Accessibility of the server option and check the Activate OPC UA Server box.

5. In the same OPC UA window, find Server addresses, where you will find the IP address you need to connect to for communication.

6. In the same window, you can allow or remove server channel permissions as needed.

7. In this example, all permissions will be disabled except for No security.

8. Finally, you can now compile the PLC to verify which license should be selected in the PLC's Runtime Licenses window.