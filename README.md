# MS-Picker

## Introduction 介紹
*MS-Picker for precise compound quantification. MS-Picker specifically generates a theoretical isotope pattern and compares the generated pattern with the observed isotope pattern in the LC-MS/M raw file. By directly comparing with the theoretical isotope pattern, the accuracy of the observed isotope pattern can be more sure , which reduces the risk of wrong removal of isotope peaks, is beneficial to the removal of isotope peaks, and can also be used for noise estimation to further improve quantitative results. MS-Picker is written in Java, so it can realize cross-platform operation. MS-Picker takes as input LC-MS/MS raw files in mzML file format, processes the files through several common steps including denoising, deisotope, extracted ion chromatogram construction and charge state determination, and exports peaks as text files The list is formatted with peak information for m/z, retention time, isotope ratio, charge state, and abundance. The output can then be processed by subsequent alignment software tools and downstream statistical analysis.*

*MS-Picker用於精確的化合物定量。MS-Picker 特別生成理論同位素模式，並將生成的模式與 LC-MS/M原始文件中觀察到的同位素模式進行比較，透過直接與理論同位素模式比較，能夠更加確定觀察到的同位素模式的準確度，減少錯誤去除同位素峰的風險，有利於同位素峰的去除，還可用於噪聲估計，進一步改善定量結果。MS-Picker是用Java編寫，因此可以實現跨平台操作。MS-Picker 將 mzML 文件格式的 LC-MS/MS 原始文件作為輸入文件，通過幾個常見步驟處理文件，包括去噪、去同位素、提取離子色譜圖構建和電荷狀態確定，並以文本文件導出峰列表具有 m/z、保留時間、同位素比、電荷狀態和豐度的峰信息的格式。然後可以通過後續的對齊軟體工具和下游統計分析來處理輸出結果。*

## MS-Picker Workflow  MS-Picker工作流程
![image](https://github.com/ICMOL/MS-Picker/blob/main/MS-Picker_workflow_ver1.png)

## How to Use 如何使用

### Input Files 輸入文件

* metabolomics or proteomics file, which is convert to mzML file by ProteoWizard MSConvert.
* Input data in **mzML** file format.
* 代謝組學或蛋白質組學文件，由 ProteoWizard MSConvert 轉換為 mzML 文件。
* 以 **mzML** 文件格式輸入數據。
### System Requirement 系統要求
* [Java SE Runtime Environment 15(or above)](https://www.oracle.com/java/technologies/javase/jdk15-archive-downloads.html)

## Step 1. Open command line 打開命令提示字元

## Step 2. Start MS-Picker and input parameter 啟動MS-Picker並輸入參數
* Input in order and separated by a space bar 1. Java startup command: java -jar MSPicker.jar 2. To input metabolomics or proteomics, separate them with 0 and 1 respectively 3. Input file folder address, you can enter single or multiple mzML file 4. Output file address 5. Required mztol (ex: 0.02)
* Input single file example: java -jar C:\Users\MS_Picker.jar 1 X:\Users\demo_data\test.mzML X:\james\demo_data\output 0.02
* Input multiple file example: java -jar C:\Users\MS_Picker.jar 1 X:\Users\demo_data\*.mzML X:\james\demo_data\output 0.02
* 依序輸入，並以空白鍵分隔1.Java啟動指令: java -jar MSPicker.jar 2.要輸入metabolomics或proteomics，分別以0和1區分 3.輸入的檔案資料夾位址，可以輸入單一或多個mzML檔案 4. 輸出檔案位址5.所要求的mztol (ex: 0.02)
* 輸入單一檔案範例: java -jar C:\Users \MS_Picker.jar 1 X:\Users\demo_data\test.mzML X:\james\demo_data\output 0.02
* 輸入多個檔案範例: java -jar C:\Users \MS_Picker.jar 1 X:\Users\demo_data\*.mzML X:\james\demo_data\output 0.02
![image](https://github.com/ICMOL/MS-Picker/blob/main/MS-Picker_cmd1.png)


## Step 3. Run MS-Picker 執行MS-Picker
*Execute MS-Picker, the execution process will display execution steps and execution time.*

*執行MS-Picker，執行過程會顯示執行到的步驟與執行時間。*
![image](https://github.com/ICMOL/MS-Picker/blob/main/MS-Picker_cmd2.png)

## Step 4. view result 察看結果
*Go to the output folder and open the output txt file to view result, which can be opened with excel.*

*到output的資料夾中打開輸出的txt檔案查看結過表格，可用excel打開。*
![image](https://github.com/ICMOL/MS-Picker/blob/main/MS-Picker_txt1.png)
