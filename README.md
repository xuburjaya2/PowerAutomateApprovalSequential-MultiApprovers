

# Power Automate 2 dynamic approver - 1 static PIC Approver - Approver by Category - Approver by DIC
### Step 1
Buat SP List dengan nama seperti ini : **Approvers - Virtual Card**

<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Approvers</td>  <td>Person or Group</td> <td> Set "allow multiple selections" for column to true. Set "Show profile photos" to true.</td> </tr>
</table>
**input nama kategori pada title dan sampel penyetuju pada list.** <br><br> 

### Step 2
Buat SP List dengan nama seperti ini : **Approvers DIC - Virtual Card**

<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Approvers</td>  <td>Person or Group</td> <td> Set "allow multiple selections" for column to true. Set "Show profile photos" to true.</td> </tr>
</table>

**input nama kategori pada title dan sampel penyetuju pada list.** <br><br> 




### Step 3
Create a SP list with the following name: **DB - Virtual Card**

<table>
  <th>Column Name</th>  <th>Column Type</th>    <th>Required</th> <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>Yes</td><td>This will be the default column that gets created in a SharePoint list</td> </tr>
<tr> <td>Amount(Rp)</td>  <td>Currency</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>No. PR</td>  <td>Number</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Alasan Pengajuan</td>  <td>Multi lines of Text</td> <td>Yes</td><td>  </td> </tr> 
<tr> <td>Req. Payment</td>  <td>Multi lines of Text</td> <td>Yes</td><td>  </td> </tr>  
<tr> <td>No. Rekening</td>  <td>Number</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Nama Pemilik</td>  <td>single line of text</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Nama Bank</td>  <td>single line of text</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Cabang</td>  <td>single line of text</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Head Office</td>  <td>single line of text</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Area</td>  <td>single line of text</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>PIC PIN</td>  <td>Person or group</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Dept head</td>  <td>Person or group</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Div Head</td>  <td>Person or group</td> <td>Yes</td><td>  </td> </tr>
<tr> <td> Amount Range </td>  <td>Lookup</td><td>Yes</td> <td> Lookup Title column of " Amount Range " list created earlier. To create lookup column go to list settings.  </td> </tr>
<tr> <td> Director In Charge </td>  <td>Lookup</td><td>Yes</td> <td> Lookup Title column of " Director In Charge " list created earlier. To create lookup column go to list settings.  </td> </tr>
<tr> <td>Approval History</td>  <td>Multi lines of Text</td><td>No</td>  <td>  </td> </tr>
<tr> <td>Approval Status</td>  <td>Choice</td><td>No</td> <td> Set Choice values as 'New, Approved, Pending, Rejected'. Set Default value of column to New. </td> </tr>
<tr> <td>Approver Index</td>  <td>Number</td> <td>No</td> <td> Set "Number of decimal places" for column to 0. </td> </tr>
<tr> <td>Approvers</td>  <td>Person</td> <td>No</td> <td> Set "allow multiple selections" for column to true. Set "Show profile photos" to true. </td> </tr>
<tr> <td>No. Ticket</td>  <td>single line of text</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>Created Date</td>  <td>Date and time</td> <td>Yes</td><td>  </td> </tr>
<tr> <td>End Date</td>  <td>Date and time</td> <td>Yes</td><td>  </td> </tr>
</table>

Ensure all of the columns mentioned in the above table + "Created By" column are a part of the "All Items" View. <br> <br> 


### Step 4
Go to Power Automate (flow.microsoft.com) and import the following flow:<br> 
[Import flow](https://github.com/xuburjaya2/PowerAutomateApprovalSequential-MultiApprovers/blob/master/Flow%20Approval/Approval%20sequential%20with%20Formsharepointlist-email-attachment.zip). <br> <br>
Once imported, ensure you update all the SharePoint actions to point to your newly created lists.  <br> 
Make sure to turn the flow on.<br><br>
If Import fails then click on "Save as a new flow" link option in error message.
