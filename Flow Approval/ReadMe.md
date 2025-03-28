

# Power Automate 2 dynamic approver - 1 static PIC Approver - Approver by Category - Approver by DIC

### Diagram Alur pada Power Automate ini :<br>
![Diagram Flow Multi-Approvals](https://github.com/user-attachments/assets/19a674de-fa5f-4806-a62b-d4dc9fc296aa)




### Step 1

![SP List approvers cat](https://github.com/user-attachments/assets/e979eb0f-1d12-4bf6-9171-fcc75e2125fb)

Buat SP List dengan nama seperti ini : **"Approvers - Virtual Card"**

<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Approvers</td>  <td>Person or Group</td> <td> Set "allow multiple selections" for column to true. Set "Show profile photos" to true.</td> </tr>
</table>
**input nama kategori pada title dan sampel penyetuju pada list.** <br><br> 

### Step 2

![SP List approvers DIC](https://github.com/user-attachments/assets/83b55502-bb8c-424d-812b-6cbe854025c7)

Buat SP List dengan nama seperti ini : **"Approvers DIC - Virtual Card"**

<table>
  <th>Column Name</th>  <th>Column Type</th>  <th>Comments</th> 
  <tr> <td>Title</td>  <td>Single line of Text</td> <td>This will be the default column that gets created in a SharePoint list</td> </tr>
  <tr> <td>Approvers</td>  <td>Person or Group</td> <td> Set "allow multiple selections" for column to true. Set "Show profile photos" to true.</td> </tr>
</table>

**input nama kategori pada title dan sampel penyetuju pada list.** <br><br> 




### Step 3
![DB-vicard 1](https://github.com/user-attachments/assets/8e5ac629-2f39-4eb7-9467-cd61d5840fd7)
![DB-vicard 2](https://github.com/user-attachments/assets/a77c6872-9dc0-47b6-b4af-c5aacc4f6c7a)
![DB-vicard 3](https://github.com/user-attachments/assets/3ff48caf-a3e8-4b64-8852-cd800e1fb5e4)
![DB-vicard 4](https://github.com/user-attachments/assets/f05ea620-3c37-4516-9a9c-1e0e8ccdb541)

Buat SP List dengan nama seperti ini:  **"DB - Virtual Card"**

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

Pastikan semua kolom yang disebutkan dalam tabel di atas + kolom "Dibuat Oleh" adalah bagian dari Tampilan "Semua Item". <br> <br> 

### Step 4
Buat formulir dari sharepoint list ikuti langkah langkah pada foto dibawah ini :
![step make form](https://github.com/user-attachments/assets/755b3525-1835-48fd-955f-763b9e1f54a9)
![step make form2](https://github.com/user-attachments/assets/7713fed0-7243-4b25-9bfa-2b2c86c87700)
![step make form3](https://github.com/user-attachments/assets/0e785469-1cae-489c-91f4-b1319327bf79) <br><br>

Hasil formulirnya seperti ini : <br>
![form list 1](https://github.com/user-attachments/assets/8893fc52-20ad-48ea-b460-ba8244493d1e)
![form list 2](https://github.com/user-attachments/assets/c096a63b-d05b-48a7-bf99-5c9de89fc823)



### Step 5
Buka Power Automate (flow.microsoft.com) dan import flow berikut:<br> 
[Import flow](https://github.com/xuburjaya2/PowerAutomateApprovalSequential-MultiApprovers/blob/4788e215d50f76596bb0d256cdc361537aeba85f/Flow%20Approval/ApprovalSequentialwithtriggerformSPlist_20250326082449.zip). <br> <br>
Setelah diimport, pastikan Anda memperbarui semua tindakan SharePoint untuk menunjuk ke daftar yang baru Anda buat.  <br> 
Pastikan untuk menyalakan alirannya.<br><br>
Jika Impor gagal maka klik opsi tautan "Save as a new flow" dalam pesan kesalahan.
