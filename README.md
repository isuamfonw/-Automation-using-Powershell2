<h><b>Introduction</b></h><br/>

In this task, I created two PowerShell scripts. PowerShell enables administrators to perform administrative tasks on both local and remote systems. I managed an Active Directory and SQL Server within the PowerShell environment. This management included the configuration and administration of the servers.
<br/>

Goal: Writng and Implementing scripts that automate configuration tasks for an orgaization.


Steps 1

- Created a PowerShell script and named it “Restore-AD.ps1” within “Requirements2” folder
- Check for the existence of an Active Directory Organizational Unit (OU) named “Finance.” Output a message to the console that indicates if the OU exists or if it does not. If it already exists, delete it and output a message to the console that it was deleted.

- Create an OU named “Finance.” Output a message to the console that it was created.

- Import the financePersonnel.csv file (found in the attached “Requirements2” directory) into your Active Directory domain and directly into the finance OU. Be sure to include the following properties:

  First Name, Last Name, Display Name (First Name + Last Name, including a space between), Postal Code, Office Phone, Mobile Phone

- Include this line at the end of your script to generate an output file for submission:

  Get-ADUser -Filter * -SearchBase “ou=Finance,dc=consultingfirm,dc=com” -Properties DisplayName,PostalCode,OfficePhone,MobilePhone > .\AdResults.txt
  <br/>
<img src ="https://tools.corenexis.com/image/cnxm/M24/12/32fddc5b83.webp" height="80%" width="80%" alt="Home page"/>


 Step 2

- Create a PowerShell script named “Restore-SQL.ps1” within the attached “Requirements2” folder. Create a comment block and include your first and last name along with your student ID.

- Write the PowerShell commands in a script named “Restore-SQL.ps1” that perform the following functions without user interaction:

- Check for the existence of a database named ClientDB. Output a message to the console that indicates if the database exists or if it does not. If it already exists, delete it and output a message to the console that it was deleted.

- Create a new database named “ClientDB” on the Microsoft SQL server instance. Output a message to the console that the database was created.

- Create a new table and name it “Client_A_Contacts” in your new database. Output a message to the console that the table was created.

- Insert the data (all rows and columns) from the “NewClientData.csv” file (found in the attached “Requirements2” folder) into the table created in part D3.

- Include this line at the end of your script to generate the output file SqlResults.txt for submission:
    Invoke-Sqlcmd -Database ClientDB –ServerInstance .\SQLEXPRESS -Query ‘SELECT * FROM dbo.Client_A_Contacts’ > .\SqlResults.txt

Apply exception handling using try-catch

<img src ="https://tools.corenexis.com/image/cnxm/M24/12/b3efffd6be.webp" height="80%" width="80%" alt="Home page"/>


<img src ="https://tools.corenexis.com/image/cnxm/M24/12/1f042ba376.webp" height="80%" width="80%" alt="Home page"/>


<img src ="https://tools.corenexis.com/image/cnxm/M24/12/50f0c72b0e.webp" height="80%" width="80%" alt="Home page"/>
