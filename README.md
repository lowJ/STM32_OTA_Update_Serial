# STM32_OTA_Update_Serial
Wifi based serial monitor and flasher for the STM32 BluePill
Flashing done using the UART bootloader on the STM32.


Serial Monitor
  - ESP32 will host a TCP socket server
  - Users can connet to the server using Netcat
  - The ESP32 will check for any TCP packets from the user and forward them to the STM32 over UART
  - The ESP32 will check for any UART messages from the STM32 and forward them to the User over TCP

Flashing
  - ESP32 will host a fileserver, and users can access it through a browser
  - Once flashing is started the STM32 gets put into Bootloader mode and the ESP32 starts flashing the binary.


  - File server and flashing component are from here: https://github.com/ESP32-Musings/OTA_update_STM32_using_ESP32




Useful Links
STM32 Bootloader Notes - https://www.st.com/resource/en/application_note/an2606-stm32-microcontroller-system-memory-boot-mode-stmicroelectronics.pdf
STM32 USART Bootloader - https://www.st.com/resource/en/application_note/an3155-usart-protocol-used-in-the-stm32-bootloader-stmicroelectronics.pdf
esp-idf TCP Server Example - todo
