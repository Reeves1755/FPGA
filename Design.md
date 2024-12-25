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

1. 暫存器檔案  
![image](https://github.com/user-attachments/assets/b1c6b271-b358-4b82-a1ac-4ade43bd3bbd)  
![image](https://github.com/user-attachments/assets/c6b29a8c-8327-4494-92f4-5f0498d390f7)
![image](https://github.com/user-attachments/assets/6b51d6d5-55af-49bb-b9bc-e85920c15a80)

2. 記憶體  
![image](https://github.com/user-attachments/assets/3b2f40ff-3f71-4e7f-84b6-a20108e433b1)  
![image](https://github.com/user-attachments/assets/9155d755-bf82-4778-912e-8b8bbbeca27f)
![image](https://github.com/user-attachments/assets/2a13adb6-9e52-4e36-afb4-20191bcb3423)

資料運算單元的效能
==
![image](https://github.com/user-attachments/assets/58b5afa5-c25d-42a6-8ac2-c3a2f00fcacb)  
![image](https://github.com/user-attachments/assets/07a21bca-afd7-406e-81e1-7d271a5100ab)  
![image](https://github.com/user-attachments/assets/61d7900c-949d-4525-84ef-83a7657212c8)  
![image](https://github.com/user-attachments/assets/87cb0cf7-0d6c-4a8d-a153-8ef0ad6fe68f)  
![image](https://github.com/user-attachments/assets/a2783680-5f83-49e1-b4db-a7e58c23e7a2)

邏輯合成原理 --> 時間限制
==
![image](https://github.com/user-attachments/assets/3bfb7419-76ac-4288-b55d-6f57a4bfebcb)  
![image](https://github.com/user-attachments/assets/6ab4463a-04da-4fe5-8cd6-fd1b69ec69fe)

管線化架構
==
![image](https://github.com/user-attachments/assets/bff33aa9-426d-41e6-9283-a2c84260549a)  
![image](https://github.com/user-attachments/assets/4468587b-2adb-4f9f-a768-48569d7dc797)  
![image](https://github.com/user-attachments/assets/7011d259-d122-4657-92cf-96674ef57b05)  
![image](https://github.com/user-attachments/assets/9fe6d893-ab94-488b-b22e-917566962a5f)  
![image](https://github.com/user-attachments/assets/20fcdb5d-ba2a-4ee9-a756-78ca31e08f59)
![image](https://github.com/user-attachments/assets/8e59ef54-9e8a-412b-8ebe-b76233336e73)  
![image](https://github.com/user-attachments/assets/cae5b117-424c-4697-a065-d8d0aba00f4b)

數位系統設計方法
==
分為資料運算單元(資料運算 --> 組合邏輯 + 儲存元件)以及控制單元(整個系統的控制流程)  
![image](https://github.com/user-attachments/assets/34bf066a-c15c-4140-a9f4-5cf15bec7625)  
![image](https://github.com/user-attachments/assets/c08f82db-276d-462d-a87e-6949eb9c13a1)  
![image](https://github.com/user-attachments/assets/279b90d4-fec6-4c5f-9590-6845dcc6627a)  
![image](https://github.com/user-attachments/assets/bd782b0f-eb69-4b2a-b5c8-4379b2cda793)
![image](https://github.com/user-attachments/assets/b325dc56-173a-4755-99b4-afb5ff861c9b)  
![image](https://github.com/user-attachments/assets/e2df6a24-5bba-4761-b17b-2e534d7510d7)  
![image](https://github.com/user-attachments/assets/aef22707-af4f-4766-9e02-aff532f94f6d)  
![image](https://github.com/user-attachments/assets/2f562706-ad9b-4545-b1fe-fac9ab95bb27)  
![image](https://github.com/user-attachments/assets/94708c18-86f7-41e9-bc54-274062b3d941)  
![image](https://github.com/user-attachments/assets/afc0d981-575d-4315-aa11-f5c52c83a748)


