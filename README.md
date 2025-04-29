# Introduction
MS-Picker is a software tool designed to detect peaks in metabolomics datasets obtained from the LC-MS platform. It performs noise reduction, de-isotoping, and extracted ion chromatogram (XIC) construction, following the algorithms detailed in [1]. The tool outputs the m/z, retention time, charge states, and intensities of the detected features.

# System Requirement
* [Java SE Runtime Environment 15(or above)](https://www.oracle.com/java/technologies/javase/jdk15-archive-downloads.html)

# Parameter Description

|parameter|description|
| ------------- | ------------- |
|mzTol| The m/z tolerance for detecting a peak.|
|input_file| The location of mzML files to be processed.|
|output_folder| The location of output files (a peak list corresponds to an mzML file.|


# How to Use
* **For a single mzML file**
<blockquote>
    java -jar MS-Picker.jar mzTol output_folder input_file<br>
    <blockquote>
    e.g., java -jar MS-Picker.jar 0.02 D:\output_folder D:\test1.mzML
    </blockquote>
</blockquote>
    
* **For mltiple mzML files**
<blockquote>
    java -jar MS-Picker.jar mzTol output_folder input_file1 input_file2 input_file3<br>
    <blockquote>
    e.g., java -jar MS-Picker.jar 0.02 D:\output_folder D:\test1.mzML D:\test2.mzML D:\test3.mzML<br>
    </blockquote>
    java -jar MS-Picker.jar mzTol output_folder input_folder_path\*.mzML<br>
    <blockquote>
    e.g., java -jar MS-Picker.jar 0.02 D:\output_folder D:\*.mzML
    </blockquote>
</blockquote>

# References
1. Chang H-Y, Chen C-T, Lih TM, Lynn K-S, Juo C-G, Hsu W-L, et al. (2016) iMet-Q: A User-Friendly Tool for Label-Free Metabolomics Quantitation Using Dynamic Peak-Width Determination. PLoS ONE 11(1): e0146112. https://doi.org/10.1371/journal.pone.0146112
