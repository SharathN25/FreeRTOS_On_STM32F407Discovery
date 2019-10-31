# Seeting up FreeRTOS on STM32F407 Discovery Kit
1. Open Keil uVision IDE. Click on **project** the select **New uVision Project.. **. Then select your working directory and give your preferred project name.
2. Now Select the device, in our case **STM32F407VG** MCU.
<img src = "FreeRTOS_Setup_Images/Figure_FreeRTOS_Basic_DeviceSelect.PNG" width="750" height="480" hspace="80" >

3. Now in the **Manage Run-Time Environment** Tab, make sure you select all the necessary driver/libraries as given below. Make sure you click **Resolve** after selecting all. 
<img src = "FreeRTOS_Setup_Images/Figure_FreeRTOS_Basic_RunTime.PNG" width="750" height="480" hspace="80">

4. Under Target1 add new Group **FreeRTOS**. Add all necessary FreeRTOS files to this group. As shown below:
<img src = "FreeRTOS_Setup_Images/Figure_FreeRTOS_Basic_Files.PNG" width="600" height="500" hspace="130">

   Path to find these files in FreeRTOS folder: 

   * **Files** : (croutine, event_groups, list, queue, stream_buffer, tasks, and timers)
 
     **Path** :  FreeRTOSv10.2.1\FreeRTOS\Source
 
   * **Files**: heap_4 ( You can add anyone memory management scheme of your choice) 
 
     **Path** : FreeRTOSv10.2.1\FreeRTOS\Source\portable\MemMang

   * **Files**: port.c (this is an MCU specific file)
 
     **Path** : FreeRTOSv10.2.1\FreeRTOS\Source\portable\RVDS\ARM_CM4F 

**Note**: FreeRTOS version may change. Just use the latest version available.

5. Now you need to add the path of all header files that are required. To do so, Right Click on **Target1**-> **Option for Target "Target1.."** -> **C/C++** -> **Include path**. Make sure you inclue these paths : 

   * Include folder in FreeRTOS ( ......\FreeRTOSv10.2.1\FreeRTOS\Source\include)
   * RVDS directory (.......\FreeRTOSv10.2.1\FreeRTOS\Source\portable\RVDS\ARM_CM4F)

<img src = "FreeRTOS_Setup_Images/Figure_FreeRTOS_Basic_IncludePath.PNG"  width="750" height="480" hspace="80" >

   **Note** : If you have any header files, make sure you include the path of these header files as explained above.

6. FreeRTOS has one important header file called **FreeRTOSConfig.h**. This file contains the application-specific(in our case-specific to Cortex M4F MCU) customization. For simplicity, I have copied our MCU specific "FreeRTOSConfig.h" file in the **RVDS** directory also in step5 we have already added RVDS path. IF you're adding it yourself then You have to add this file in your project and also make sure you include the path of this file as explained in step 5. 

7. Now under User Application Group add a new **C file**. In the repository **main.c** file has the basic template so that the FreeRTOS application compiles successfully.  So please use this basic code in the main function for the successful compilation of the FreeRTOS application.

<img src = "FreeRTOS_Setup_Images/Figure_FreeRTOS_Basic_MinnimalCfile.png"  width="750" height="480" hspace="80" >


