Download Link: https://assignmentchef.com/product/solved-embsys100-module-7-cortex-microcontroller-software-interface-standard
<br>
The goals for the assignment this week:

<ol>

 <li>Practice the use of the Cortex Microcontroller Software Interface Standard (CMSIS).</li>

 <li>Gain more practice with the Cortex-M4 assembly language.</li>

 <li>Become familiar with the linker Map file and use it to determine the resource usage.</li>

</ol>

Problems:

<ol>

 <li>Use the CMSIS to implement code that blinks the user LED on the STM32 board.

  <ol>

   <li>Create a new project.</li>

   <li>Create a main.c file and add it to the project.</li>

   <li>Add the files “<strong>h</strong>” &amp; “<strong>system_stm32f4xx.h</strong>” to the folder where “main.c” is saved. <em>You should be able to get these files thru STM32CubeMX. You could also get them by downloading the zip file “CMSIS_STM32_Device_Specific_Files.zip” from canvas site under the link </em><a href="https://canvas.uw.edu/courses/1325909/files/folder/EMBSYS%20100%2019/Assignments/A06"><em>Assignment</em></a><a href="https://canvas.uw.edu/courses/1325909/files/folder/EMBSYS%20100%2019/Assignments/A06"><em></em></a><a href="https://canvas.uw.edu/courses/1325909/files/folder/EMBSYS%20100%2019/Assignments/A06"><em>A06 folder</em></a></li>

   <li>Enable use of CMSIS in project options settings.</li>

   <li>Implement toggling of the LED using the CMSIS data structures.</li>

  </ol></li>

</ol>

<ol start="2">

 <li>Convert the blinking led program into assembly code.

  <ol>

   <li>Go to the link <a href="https://canvas.uw.edu/courses/1325909/files/folder/EMBSYS%20100%2019/Assignments/A06">Assignment</a><a href="https://canvas.uw.edu/courses/1325909/files/folder/EMBSYS%20100%2019/Assignments/A06"></a><a href="https://canvas.uw.edu/courses/1325909/files/folder/EMBSYS%20100%2019/Assignments/A06">A06 folder</a> and download the zip file</li>

  </ol></li>

</ol>

“<em>Module07_Assignment06_Starter_Code.zip</em>”. Use the skeleton files (<strong>main.c</strong>, <strong>user_led.s</strong>, and <strong>delay.s</strong>) inside that zip file.

<ol>

 <li>Create a new project and add the skeleton files to that project.</li>

 <li>Make sure to setup the project to connect to your board (follow instructions form <strong>Module_02</strong> if you forgot how to do that).</li>

 <li>Implement the function <strong>control_user_led</strong> in assembly.

  <ol>

   <li>The function takes as input the led requested state (0 == OFF, 1 == ON) and the duration for holding the state.</li>

   <li>The function returns void.</li>

  </ol></li>

 <li>Implement the function <strong>delay</strong> in assembly

  <ol>

   <li>The function takes as input an integer value.</li>

   <li>The function will decrement the value until it reaches 0</li>

  </ol></li>

</ol>

<ul>

 <li>Then returns void.</li>

</ul>

<ol>

 <li>Call the “control_user_led” function from a while loop in main.</li>

 <li>For any C code, use only data types defined in the “stdint.h” file</li>

</ol>




<u>Hints:</u>

<ol start="4">

 <li>Implement delay in assembly first. Once it works, implement control_user_led function.</li>

 <li>Use your simple LED code that made use of the peripheral registers (<strong>not</strong> the bit-banding registers).</li>

 <li>It is ok to use a hard code value of the ODR (Output Data Register) address for GPIOA and store it into one of the CPU scratch registers.</li>

 <li>Generate the map file for your program and provide details on:

  <ol>

   <li>How much total ROM your program is occupying?</li>

   <li>How much total RAM your program is using?</li>

   <li>What part of your program is using the most ROM?</li>

   <li>What part of your program is using the most RAM?</li>

  </ol></li>

 <li><strong><u>Bonus:</u></strong> Anything that can be done to optimize the usage of ROM or RAM resources? Explain any options.</li>

 <li><strong><u>Bonus:</u></strong> Re-implement the <strong>control_user_led</strong> to use the bit-band region for accessing the Output Data Register (ODR) for GPIOA in order to toggle the LED ON/OFF. <u>Hint:</u> It is ok to use a hard code value of the ODR bit-band address for GPIOA and store it into one of the CPU scratch registers.</li>

</ol>