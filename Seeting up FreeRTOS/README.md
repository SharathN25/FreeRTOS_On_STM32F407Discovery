# Seeting up FreeRTOS on STM32F407 Discovery Kit
1. Open Keil uVision IDE. Click on **project** the select **New uVision Project.. **. Then select your working directory and give your preferred project name.
2. Now Select the device, in our case **STM32F407VG** MCU.
<img src = "FreeRTOS_Setup_Images/Figure_FreeRTOS_Basic_DeviceSelect.PNG" width="750" height="480" hspace="80" >

3. Now in the **Manage Run-Time Environment** Tab, make sure you select all the necessary driver/libraries as given below. Make sure you click **Resolve** after selecting all. 
<img src = "FreeRTOS_Setup_Images/Figure_FreeRTOS_Basic_RunTime.PNG" width="750" height="480" hspace="80">

4. Under Target1 add new Group **FreeRTOS**. Add all necessary FreeRTOS files to this group. As shown below:
<img src = "FreeRTOS_Setup_Images/Figure_FreeRTOS_Basic_Files.PNG" width="600" height="500" hspace="130">
