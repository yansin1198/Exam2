# Exam2

Setup
  
  1.Download Files or git clone https://github.com/yansin1198/hw3.git
  2.In the file, add "4DGL-uLCD-SE" library: 
  git clone https://gitlab.larc-nthu.net/ee2405_2021/4dgl-ulcd-se.git
  3.In the file, add a library for decoding: (BSP library is also needed)
  mbed add https://gitlab.larc-nthu.net/ee2405_2021/tensorflowlite_mbed
  $ cp -r ~/ee2405/<library路徑>/src/data_collect/BSP_B-L475E-IOT01.
  4.In the file, add RPC Library: 
  mbed add https://gitlab.larc-nthu.net/ee2405_2021/mbed_rpc.git
  5.In the file, add MQTT: 
  mbed add https://gitlab.larc-nthu.net/ee2405_2019/wifi_mqtt.git
  6.Modify mbed_app.json contents (SSID、PSSWORD)
  7.Modify main.cpp and mqtt_client.py IP address
  
Compile

  1. Open terminal:
     $ mkdir -p ~/ee2405new
  2. cp -r ~/ee2405/mbed-os ~/ee2405new
  3. mbed compile --library --no-archive -t GCC_ARM -m B_L4S5I_IOT01A --build ~/ee2405new/mbed-os-build2 (這一步要在ee2405new裡面做)
  4. sudo mbed compile --source . --source ~/ee2405new/mbed-os-build2/ -m B_L4S5I_IOT01A -t GCC_ARM -f 去compile作業3
  5. sudo screen /dev/ttyACM0
  6. Open the other terminal to finish connect:
     sudo python3 wifi_mqtt/mqtt_client.py
     
Result
  Please see the screenshot in files
