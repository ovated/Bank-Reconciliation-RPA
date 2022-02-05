<h2> Bank-Reconciliation-RPA</h2>
<body>

Python script to Automate a Bank Reconciliation process in excel.

<h3>Business rules:</h3>

Note: There are two excel sheets for this automation process; Bank sheet, and sage sheet.
<ol>
<li>
Compare the first bankrow price, with all the rows in the sage sheet, if the prices column of both sheets match, reconcile the bank row. If the bank price does not match with any row in the sage sheet, add the row number to unreconciled row list.
</li>
<li>
If both prices match, the dates dont match, the bank row to unreconciled bank row list.
</li>
<li>
If the bank price does not match any sage row;
	Get the bank transaction description, compare it to the sage transaction descriptions.
	If the bank and sage price match, and the bank and sage date match, reconcile.
	If transaction description matches, but prices do not match;
		If the bank price is greater than the sage price;
			Find all the transaction description matches in sage, add them up together, and compare with the bank price.
			If they match, reconcile bank row.
			If they do not match, check if the bank price is greater than the total sage price.
			If True reconcile,
			If False;
				Add up all the rows in the bank sheet that contains the the same bank transaction description.
				And compare the total bank price to the total sage price.
				If they match reconcile.
				

</li>
    
</ol>
    
</body>

Paste the unreconciled bank sheets to the unposted bank sheet.
