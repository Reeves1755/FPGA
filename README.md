FPGA
===
Created by Reevex\
source : yt --> FPGA系統設計實務_蕭宇宏
---
硬體描述語言
---
Hardware Description Language (HDL)  
輔助硬體(電路)設計的語言  
藉由描述硬體的介面、功能行為、時序來設計  
模擬硬體的結果用於驗證功能  
需搭配EDA tool 將HDL轉換成電路(合成Synthesis)  
需PC or 工作站作為平台進行設計
主要支援半客戶式(Semi-custom)的設計方法  

Why HDL?
---
1. 電路(系統)越來越大 幾百萬電晶體在單一晶片 功能複雜度高 設計困難 驗證困難
2. 尋求簡單且快速的設計過程 驗證簡單
3. 尋求較大的解決問題空間 --> 各種可能性的評估

HDL 特色
---
1. 支援不同硬體層級描述![image](https://github.com/user-attachments/assets/0b9c6a74-3af9-4d38-b6a1-6cf1cc6be096)  
2. 支援階層式設計(模組化)![image](https://github.com/user-attachments/assets/ebfabbb7-c0bc-41b6-b587-872252de8c37)  
3. 藉由EDA tool輔助設計  
  - 合成工具
    - 行為描述轉換成電路
    - 預測電路的成效(速度、成本、功耗)
    - 最佳化
  - 模擬工具
    - 模擬電路行為
  - 驗證工具  
    - 自動化功能驗證
4. 可重複使用
  - 模組化設計
  - 參數化設計
  - 可與後段製程無相關(Portable 可攜帶性) --> 不必因為製程改變就重新設計
  - Soft IP --> 使用已設計好的模組

主要的HDL有VHDL、Verilog

微處理器與FPGA的差別
---
1. 可程式化的差異
![image](https://github.com/user-attachments/assets/3dfa3e67-f0f0-4582-bfc8-1fbc145b3428)  
2. 語言的差異
   - 微處理器
     - 軟體語言  
         高階：Basic、C、C++、Java  
         低階：組合語言、機器語言(0與1)
     - CPU透過一連串指令來運作
   - FPGA
     - 硬體描述語言(VHDL、Verilog)
     - 描述硬體的架構行為
     - 合成工具實現電路
3. 執行效能的差異
   - 微處理器
     - 只有一套運算單元(單核心) --> 一連串指令依序排隊來完成
     - 一個指令通常需要多個硬體程序來完成
   - FPGA
     - 可以規畫多個單元 --> 運算可以並行處理
     - 效能可以達到最佳化
