### EXPERIMENT -07 CONFIGURING NETWORK SERVER FOR CONNECTING GATEWAY AND END NODE 
 
## Aim: 
To  configure the Network server and end device for transferring data on the network
## Components required: 
End node stm 32 development kit , Dragino LPS8, Network server 

## Theory :
When working with sensitive applications or files, saving progress on your local device is a start, but what if you lose access to your device? Network servers address this problem by hosting the files and programs most pertinent to the network and enabling access for consistent, real-time use. 

As a result, personnel or network clients can instantly access important data or tools while also facilitating collaboration between users. Multiple users can make changes to the same program or document for continued development over the course of a project. Via a secure login, remote users can connect to the home network.
![image](https://github.com/vasanthkumarch/EXPERIMENT-07-CONFIGURING-NETWORK-SERVER-FOR-CONNECTING-GATEWAY-AND-END-NODE-/assets/36288975/59db9b76-ddd5-4d6a-9075-8db233f5e479)


In the above graphic, the circle represents an organization network where a network server facilitates collaboration and file sharing between network clients (devices).

 The role of a network server, then, is to provide users with a set of services and access to resources on the network. These features include:

Permissioned access and log-ins for network users Gateway access to the Internet for an organization Centralized location for network resources  Shared access to devices on the network like a printer or a scanner Hosts multi-user apps like email servers, web applications, or CRM

## Procedure :

 1. login to the network server using login link  https://iot.saveetha.in/
 2. Click on the nework server as shown blow
    
 ![image](https://github.com/vasanthkumarch/EXPERIMENT-07-CONFIGURING-NETWORK-SERVER-FOR-CONNECTING-GATEWAY-AND-END-NODE-/assets/36288975/1bd434ca-1426-4102-8384-94473483543e)
 3. Click on the add gateway 
 
 ![image](https://github.com/vasanthkumarch/EXPERIMENT-07-CONFIGURING-NETWORK-SERVER-FOR-CONNECTING-GATEWAY-AND-END-NODE-/assets/36288975/47c2e08d-6598-4437-8b07-f213d6f3b8ac)
![image](https://github.com/vasanthkumarch/EXPERIMENT-07-CONFIGURING-NETWORK-SERVER-FOR-CONNECTING-GATEWAY-AND-END-NODE-/assets/36288975/e62ff028-99bc-485e-9808-fbb6e124f8b2)
![image](https://github.com/vasanthkumarch/EXPERIMENT-07-CONFIGURING-NETWORK-SERVER-FOR-CONNECTING-GATEWAY-AND-END-NODE-/assets/36288975/a2e3ae58-6402-49e8-8f96-679059c1842c)
4. Click on the lora options , lora - frequency plan 

5. Click on channels and create a new channel after which you can add a new end device
   
![image](https://github.com/vasanthkumarch/EXPERIMENT-07-CONFIGURING-NETWORK-SERVER-FOR-CONNECTING-GATEWAY-AND-END-NODE-/assets/36288975/1fb72be5-e48d-4cde-a329-0cfb0d29070f)

6. Add the attributes in the end device as  shown below 

 ![image](https://github.com/vasanthkumarch/EXPERIMENT-07-CONFIGURING-NETWORK-SERVER-FOR-CONNECTING-GATEWAY-AND-END-NODE-/assets/36288975/00bff30b-42fc-42d5-9540-285d270e41cb)
 
7.Using AT commands configure end device in serial port utility
AT Commands to set initially (Mandatory)
 AT+FDR // To do factory data reset
 AT+NJM=1 // To set OTAA mode
 AT+ADR=1 // To enable the ADR
 AT+TDC=600000 // To set the default sampling interval as 10 minutes
(Should not give below 5 minutes)
 AT+CLASS=C // To set class C
 AT+DEUI=XX XX XX XX XX XX XX XX // To set Device EUI key
 AT+APPEUI=XX XX XX XX XX XX XX XX // To set APP EUI key
 AT+APPEUI=XX XX XX XX XX XX XX XX XX XX XX XX XX XX XX XX //
To set APP Key
 ATZ // To take effective action on below settings (As like saving)



## OUTPUT 
<img width="1916" height="1021" alt="Screenshot 2025-12-01 192646" src="https://github.com/user-attachments/assets/dc869d55-94ae-44cd-bafd-c6a4c1a303f9" />
<img width="1916" height="1021" alt="Screenshot 2025-12-01 192646" src="https://github.com/user-attachments/assets/1191fbed-376b-4680-8152-2a2f6b561e6e" />
<img width="1903" height="1013" alt="Screenshot 2025-12-01 192919" src="https://github.com/user-attachments/assets/ac120a58-b973-4997-8e94-4a34be5aecaf" />
<img width="1917" height="1016" alt="Screenshot 2025-12-01 193042" src="https://github.com/user-attachments/assets/a206281c-b396-4e08-9b93-3313446fdf47" />
<img width="1907" height="1012" alt="Screenshot 2025-12-01 193130" src="https://github.com/user-attachments/assets/5fa3c460-23dc-4eee-a8b8-ac4d6200c0c4" />
<img width="1907" height="1012" alt="Screenshot 2025-12-01 193130" src="https://github.com/user-attachments/assets/e16d8d23-813c-43bd-98d8-d43fb0b115ae" />
AT COMMANDS:
<img width="1920" height="1007" alt="509443110-eaa1e55d-01d5-4d30-8580-a12e27f374e0" src="https://github.com/user-attachments/assets/b7ebe869-2b1b-4b9d-931f-2c4174f44fed" />
<img width="1920" height="1007" alt="509443202-7e310419-e4f1-4bc0-92da-d1002855866c (1)" src="https://github.com/user-attachments/assets/c12ecbeb-6eb7-4a32-89ea-e950dbd02c2a" />
<img width="1920" height="1014" alt="509443202-7e310419-e4f1-4bc0-92da-d1002855866c" src="https://github.com/user-attachments/assets/a3f89146-d381-48ac-a560-15f47d557c94" />
<img width="1920" height="1011" alt="509443295-fd794d0c-2b24-4166-bb15-2da7cfcbb333" src="https://github.com/user-attachments/assets/6621ddb5-048b-4a88-ac5a-8889ab71985a" />
<img width="1920" height="1011" alt="509443353-59a0a53c-5876-44c2-867b-57304e15b0bc" src="https://github.com/user-attachments/assets/612c7097-8ff5-4a1a-bde2-8133406e561f" />
<img width="1920" height="1021" alt="509443408-5f1e51c2-c7b7-421c-b7af-cebbb508bfe4" src="https://github.com/user-attachments/assets/b5c3e281-0e6f-4760-a6c6-34ef8554f518" />
<img width="1920" height="1017" alt="509443535-63046070-f41a-4ef5-bae1-e34113799160" src="https://github.com/user-attachments/assets/5f84eff3-c087-4152-8d14-a15354743c91" />
<img width="1920" height="1014" alt="509443615-6a87737f-a241-4f73-a71e-7d0d54af366b" src="https://github.com/user-attachments/assets/a5ec796d-f1bb-420a-a4af-eb56175d950a" />
<img width="1920" height="1014" alt="509443675-da0909dc-3343-46ea-ac67-c0422f4ef5bb" src="https://github.com/user-attachments/assets/50508bf0-274a-40ab-93aa-5a9337523342" />
<img width="1920" height="1011" alt="509443743-3341e188-09a7-4733-83a7-13ba392f0ed8" src="https://github.com/user-attachments/assets/341621e8-e272-49d3-8a26-22421414a775" />



## Result: 

  The Network server and end device for transferring data on the network has been accomplished.
