# Track End-of-Life(EOL) of IT Hardware Asset

Tracking the end-of-life data of hardware assets will help companies plan ahead, save money, and reducing security risk exposure. When it comes to ITAM(IT Asset Management),HAM(Hardware Asset Management) goes hand-in-hand with SAM(Software Asset Management). Any new software to function correctly, it needs to run on well maintained hardware.

PDQ Inventory is a systems management tool that scans **Windows** computers to collect hardware, software, and Windows configuration data. PDQ Inventory stores all of its data collections/reports, computer inventory information, Active Directory information, preferences settings, etc. in the SQLite database file.

To track EOL of hardware asset, OEM support team expects Machine Type Mode and SerialNumber data in specific format(CSV or XLS or XLSX). To accomplish this, follow the steps below:

## 1. Get Lenovo assets End-Of-Life infortmation
**Step 1.** PDQ Inventory -> Right Click on All Computers Collection -> Click on New -> Click on SQL Report

  **Name :** Lenovo-assets-file<br />
  **Description:** Optional. You can leave it Blank

**Step 2.** Copy and Paste the below SQL query to text box as below. (Clear the existing default query before  pasting)

**Step 3.** Save the Report.
      
      select
	      Computers.Model  As "Machine Type",
	      Computers.SerialNumber  As "SerailOrIMEI"
      from Computers 
      where <ComputerFilter> AND Computers.Manufacturer="LENOVO"
    
    
![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/b54653f4-83af-421b-bef7-d2b6277423a4)


**Step 4.** Run the report: Either by navigating to **File -> Run Report** OR **Blue Arrow Button on toolbar.**<br />
This will open the window with all LENOVO assets Model # and Serial # as shown below:

![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/4dc8f57f-441f-40db-b24a-dfb9061e5478)


**Step 5.** Save data to XLS file: Either by navagating to **File -> Save Data to File** OR **CSV button on toolbar.**<br />
Save as <br />
File name: Lenovo-assets-file <br />
Save as Type: Excel 97-2003 workbook(.xls)

**Step 6.** Open the link https://pcsupport.lenovo.com/us/en/warrantylookup/batchquery in any browser.<br />
Click on Browse in Upload your "File  file select" field and select above saved Lenovo-assets-file.xsl. <br />Click on SUBMIT. <br />
![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/012a44f3-73b1-4f7d-8943-50953efd98e5)

It will take some time to pull the EOL details of all the  devices.<br />

**Step 7.** Click on Export "results to Excel" and Save the Query results.<br />
![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/4bb464ea-87ab-4c3c-b182-0ac27627da21)

## 2. Get Dell assets End-Of-Life infortmation
**Step 1.** PDQ Inventory -> Right Click on All Computers Collection -> Click on New -> Click on SQL Report

  **Name :** Dell-assets-file<br />
  **Description:** Optional. You can leave it Blank

**Step 2.** Copy and Paste the below SQL query to text box as below. (Clear the existing default query before  pasting)

**Step 3.** Save the Report.
      
      select
	      Computers.SerialNumber  As "SerailOrIMEI"
      from Computers 
      where <ComputerFilter> AND Computers.Manufacturer="DELL"
    
    
![image](https://github.com/ShivuChirantana/PDQ-Handson/assets/138813405/2cf7c820-091f-4e9b-8297-873e68c32466)


**Step 4.** Run the report: Either by navigating to **File -> Run Report** OR **Blue Arrow Button on toolbar.**<br />
This will open the window with all DELL assets with Serial #.

**Step 5.** Save data to CSV file: Either by navagating to **File -> Save Data to File** OR **CSV button on toolbar.**<br />
Save as <br />
File name: Dell-assets-file <br />
Save as Type: Comma Separated Values(*.csv)

**Step 6.** Download DellWarranty-CLI.exe from https://www.dell.com/support/home/en-in/drivers/DriversDetails?driverId=63F0W and install it in your system.
It will take some time to pull the EOL details of all the  devices.<br />

**Step 7.** Search for "Dell Command Warranty" in Command search bar and  and run "Dell Command Warranty" utility. <br />
It opens the command prompt. run the below command<br />
 \> DellWarranty-CLI.exe /I=\<Absolute Path for Dell-assets-file.csv file\> /E=\<Absolute path of output file\> <br />
 Example:<br />
 \> DellWarranty-CLI.exe /I=C:\Dell-assets-file.csv /E=C:\Query-Report-Dell.csv <br />

 This command creates Query-Report-Dell.csv in C:\ path.




    



