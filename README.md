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

Verilog 的模型
---
1. 低階交換層次模型(Switch Level Model) 或電晶體模型(Transistor Model)
   Verilog最低階的模型  
   電路由開關與電晶體組成  
   一般不用來設計

2. 邏輯閘層次模型(Gate Level Model)  
   使用基本邏輯閘元件 AND OR NOT...  
   邏輯電路圖

3. 資料處裡模型(Data Flow Model)  
   描述電路中資料的處理方式  
   資料如何在電路中運算 傳送  
   輸入持續驅動輸出(assign)  
   運算式 ex: out = a + b + c

4. 行為模型(Behaviroral Model)  
   Verilog最高階的模型  
   不須考慮硬體元件特性，只須放在模組的功能描述  
   像C語言  
   需合成軟體工具
   
5. 結構式模型(Structure Level)  
   引用硬體模組的形式  
   類似邏輯閘層次模型  
   支援階層式設計法

階層式設計
---
階層概念
- 複雜電路 --> 一層疊一層的結構
- 由下而上(Bottom-up)
- 由上而下(Top-down)
- 架構上類似樹狀結構

Verilog語法詞彙
---
一連串的標記(token)所組成
- 識別字(identifiers) --> 大小寫有區別
- 關鍵字(keywords) --> 特殊名稱 所以關鍵字都用小寫 都不能當識別字 ex : always case ...
- 字串(strings) --> 一連串字元(character)組成 放在雙引號內
- 註解(comments) --> 可讀性(readability) 文件化(documentation) 版權宣告(license declaration) 
- 空白(whitespace) --> 區隔物件 除了字串內空白 註解跟空白在編譯與合成會被忽略
- 數值(numbers)
  - 固定長度(sized) --> 定義位元寬度
  - 不定長度(unsized) --> 未定義
  - 數值組(Value set) --> 0, 1, x(unknown value), z(high impedence, dloating state)

Verilog資料物件及型態
---
- 接線(nets) --> 連接線 內定值為 z
  - wire
- 暫存器(register) 內定值為 x 
  - reg
- 純量(scalar) --> 一個位元的物件
- 向量(vector) --> 多個位元
  [大數字 : 小數字]、[小數字 : 大數字] --> [MSB : LSB] 兩種都可以但左邊是最高位元  
- 陣列(array)
  - ex : 128個32bits的暫存器 --> reg [31:0] mem_block [127:0];
  - ex : 8bits的2D 4*64暫存器陣列 --> reh [7:0] mem_2D [3:0][0:63];  
- 參數(parameters) --> 常數

運算式表示
---
運算式(Expression)
  - 描述訊號與其他訊號間的關係
  - 由運算元(operand)與運算子(operator)組成
算術運算子(Arithmetic) --> 輸入為不確定值時 結果也是不確定值
![image](https://github.com/user-attachments/assets/b5218a19-7686-4eed-8c17-bd86ffbe4fc1)  
少用原因合成出的店路面機會太大 有些合成器合成不出來
位元運算子(Bit-wise) --> 兩運算元的相對應位元做邏輯運算 若兩運算元不等長 短的會補0  
![image](https://github.com/user-attachments/assets/0c7ad778-8411-431d-b246-9731d6cad813)
