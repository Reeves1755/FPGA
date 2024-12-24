Avoid latch
==
1. 設定初始值  
![image](https://github.com/user-attachments/assets/e42e067b-e6bb-4ab2-96e8-6d7743de0741)
2. default

Filp Flop
==
1. DFF  
![image](https://github.com/user-attachments/assets/7fcd41af-0a63-47ce-8e7f-71fd8a8594f5)
2. 同步重置DFF  
![image](https://github.com/user-attachments/assets/2fde82b9-eef5-4dc3-993f-0b9a7654c913)
3. 非同步重置DFF  
![image](https://github.com/user-attachments/assets/4f443682-7549-4fd9-92e4-ca70786714c8)
4. 致能DFF  
![image](https://github.com/user-attachments/assets/940b9fab-2f21-4236-89f5-4771f83847e6)

除頻器
==
1. 1/2除頻器  
   ![image](https://github.com/user-attachments/assets/3ecb4c62-32d2-4e3b-a2ad-ad9f80242f87)  
2. 1/6除頻器  
   ![image](https://github.com/user-attachments/assets/7d314894-4bfd-4144-aabd-f9d197f5e023)
   ![image](https://github.com/user-attachments/assets/5f120e30-ba8e-4f97-8a4f-511783a4471e)
   ![image](https://github.com/user-attachments/assets/eb56788b-d180-4b39-9c51-b3845507152e)
   ![image](https://github.com/user-attachments/assets/9e4e97f7-b42d-479c-b6cc-9dba9ebcba0a)
   ![image](https://github.com/user-attachments/assets/33089292-18a7-4380-8c98-b14fc92b8c4e)

彈跳現象
==
![image](https://github.com/user-attachments/assets/05fb5e42-c205-4a7f-bf54-7b61034e51d2)  
導致問題 --> 電路不穩定  
![image](https://github.com/user-attachments/assets/9be2efa7-0452-4743-836d-f230dc4ce2ab)  
目標  
![image](https://github.com/user-attachments/assets/74b0710c-f587-40cf-ac59-f5bc64e09d56)  
解法  
![image](https://github.com/user-attachments/assets/d6586f3b-e355-43ea-a31d-a44386c5b21c)  
除彈跳電路_1  
![image](https://github.com/user-attachments/assets/760c4037-c6e9-4b09-9772-d1aa1613010b)  
除彈跳電路_2  
![image](https://github.com/user-attachments/assets/fad3b842-63f9-4180-94a7-157f5f24fb6a)  

亞穩定現象(Metastable)  
需有充足的setup time & hold time  
![image](https://github.com/user-attachments/assets/c1e060c3-932a-4b0e-9d5a-b9fb87441c25)  
![image](https://github.com/user-attachments/assets/5d8ff4d5-eb00-4e9f-8ea1-27e3b85b9942)

避免Metastable  
![image](https://github.com/user-attachments/assets/52d40b2d-66ee-4cd3-923c-f1517bd7e852)  
![image](https://github.com/user-attachments/assets/613073ba-bf55-4447-ac9f-c3ba7f18b7dc)  


脈衝寬度調變
==
- Pulse Width Modulation(PWM)
- 利用脈波訊號來模擬類比訊號
   - 利用數位訊號實現
   - 利用ON/OFF調變方波 使訊號平均值改變
- 應用 : 調變光度 直流馬達控制 通訊編碼

脈寬調變原理
==
改變Duty cycle(工作週期) = 週期內ON時間 / 週期 (%)  
平均值 = Duty cycle * 最大值 (假設最小是0)  
平均值分別是2.5 V & 1.25 V  
![image](https://github.com/user-attachments/assets/a4a68119-8f78-48b2-87e3-0970aa7c2641)

脈寬調變實現
==
利用計數器實現  
透過比較器 改變 Duty cycle  
![image](https://github.com/user-attachments/assets/a9a112c9-9f28-42da-959f-4d2a4ae35002)

編譯指令(complier directive)介紹
==
1. 給編譯器看的指令
2. 編譯進行的前置設定
3. keyword --> `

- 'include  
將另一個verilog檔案包含進來進行編譯 (Quartus 不用 它會自動包含同一專案的檔案)
- 'define  
![image](https://github.com/user-attachments/assets/5c24114f-0663-4ecc-baff-21d4ffe67fd0)
- 選擇性編譯  
![image](https://github.com/user-attachments/assets/a6f9f232-f2e3-4884-8db8-fe4a74323567)  
![image](https://github.com/user-attachments/assets/bad57342-471e-4526-83b9-302687839a4d)
![image](https://github.com/user-attachments/assets/2ef49283-1f19-407f-b11a-c4305777eb48)  
![image](https://github.com/user-attachments/assets/8961f374-e48c-463c-a4d3-97643d3f2f48)  
![image](https://github.com/user-attachments/assets/c491c1f1-236b-4121-9e38-e3a1c2a36bbf)
- 'timescale  
![image](https://github.com/user-attachments/assets/815b6472-add3-48a3-9d2b-dfcbb85c51e3)

系統任務
==
![image](https://github.com/user-attachments/assets/563dab2f-661d-4d77-b311-fac9ab205052)

測試檔案介紹
==
![image](https://github.com/user-attachments/assets/d010f9e1-1e91-4b17-9064-55cb6dd92127)  

測試檔案撰寫
==
![image](https://github.com/user-attachments/assets/1e018d51-d75f-4d05-b14b-b323fe9ad1e6)

initial always比較
==
![image](https://github.com/user-attachments/assets/be676a58-7c60-46b5-a0f5-171df8eeb7e4)  
![image](https://github.com/user-attachments/assets/d5cc56fb-fb85-472f-9a81-1f51eeae0f4d)  
![image](https://github.com/user-attachments/assets/f2aec9f5-cfe9-4e45-b988-7d136c5b2fbe)  
![image](https://github.com/user-attachments/assets/d3e92c4c-d8dc-41c9-a642-9cadf67ea163)

執行測試檔案
==
![image](https://github.com/user-attachments/assets/0de11edc-5cf3-4575-8300-04a12ac8e949)

螢幕顯示系統任務
==
![image](https://github.com/user-attachments/assets/b5ea831d-6768-48c4-9b01-b9bbb01a4161)  
![image](https://github.com/user-attachments/assets/67816725-cfa9-4f8d-affe-b0dcc8c25d38)

數位系統架構
==
![image](https://github.com/user-attachments/assets/ac2a75b8-83aa-46a5-905b-10cc6acea97d)

有限狀態機
==
![image](https://github.com/user-attachments/assets/6faa14d3-2ab0-45c1-a23c-f7c573020493)  
ex  
![image](https://github.com/user-attachments/assets/8e864c34-66a9-4405-b999-cb6842588c6c)  
![image](https://github.com/user-attachments/assets/52c22b01-2640-4d1e-b2a3-00d8fa6714ac)  
推導FSM  
![image](https://github.com/user-attachments/assets/e58142fd-4bcf-4489-8e20-60995a510d64)  
狀態機類型  
![image](https://github.com/user-attachments/assets/26a482f3-1b2e-4552-8735-b6d86736847a)  
![image](https://github.com/user-attachments/assets/7dac7ba1-0f66-408c-914a-0292e4e731b0)

資料運算單元
==
![image](https://github.com/user-attachments/assets/9fa0cb87-a5bb-4c46-8a0e-9b710a4fed00)  
![image](https://github.com/user-attachments/assets/f81292d9-ca06-4d6d-ab69-160d0613fa3e)  
基本單元  
![image](https://github.com/user-attachments/assets/62db3f56-624b-4af6-8f82-f86ec72b9043)  
![image](https://github.com/user-attachments/assets/81885a5f-c0b3-41c2-a33c-455f2cae5ccc)  
![image](https://github.com/user-attachments/assets/30bd86f6-c05e-4f18-b3aa-a6bd919bdee1)  
![image](https://github.com/user-attachments/assets/d4dc9a5b-5574-46c2-ba15-640a7c26b6c0)  
![image](https://github.com/user-attachments/assets/96a8a564-cf51-4ced-ae3c-8f7c3376d281)  
範例  
![image](https://github.com/user-attachments/assets/9a176c4a-4223-41e8-8285-eaa015c0826c)  



