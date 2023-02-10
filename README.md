# MS-Picker

## Introduction
*MS-Picker用於精確的化合物定量。MS-Picker 特別生成理論同位素模式，並將生成的模式與 LC-MS/M原始文件中觀察到的同位素模式進行比較，透過直接與理論同位素模式比較，能夠更加確定觀察到的同位素模式的準確度，減少錯誤去除同位素峰的風險，有利於同位素峰的去除，還可用於噪聲估計，進一步改善定量結果。MS-Picker是用Java編寫，因此可以實現跨平台操作。MS-Picker 將 mzML 文件格式的 LC-MS/MS 原始文件作為輸入文件，通過幾個常見步驟處理文件，包括去噪、去同位素、提取離子色譜圖構建和電荷狀態確定，並以文本文件導出峰列表具有 m/z、保留時間、同位素比、電荷狀態和豐度的峰信息的格式。然後可以通過後續的對齊軟體工具和下游統計分析來處理輸出結果。*

## How to Use

### Input Files

* metabolomics or proteomics file, which is convert to mzML file by ProteoWizard MSConvert.
* Input data in **mzML** file format.

### System Requirement
* [Java SE Runtime Environment 15(or above)](https://www.oracle.com/java/technologies/javase/jdk15-archive-downloads.html)

## Step 1. Open command line

## Step 2. Start MS-Picker and input parameter
* 依序輸入，並以空白鍵分隔1.Java啟動指令: java -jar MSPicker.jar 2.要輸入metabolomics或proteomics，分別以0和1區分 3.輸入的檔案資料夾位址，可以輸入單一或多個mzML檔案 4. 輸出檔案位址5.所要求的mztol (ex: 0.02)
* 輸入單一檔案範例: java -jar C:\Users \MS_Picker.jar 1 X:\Users\demo_data\test.mzML X:\james\demo_data\output 0.02
輸入多個檔案範例: java -jar C:\Users \MS_Picker.jar 1 X:\Users\demo_data\*.mzML X:\james\demo_data\output 0.02
![image](https://github.com/ICMOL/MS-Picker/blob/main/MS-Picker_cmd1.png)


## Step 3. Run MS-Picker
執行MS-Picker


## Step 4. 察看結果
到output的資料夾中打開輸出的txt檔案
