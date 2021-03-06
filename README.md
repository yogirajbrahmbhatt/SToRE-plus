# SToRE + 
## _The easy-to-operate Billing and Stock Management Software_
- Easy billing procedure
- Perform the operations such as Add, Remove, Apply Discount etc.
- Generate the bill and Get all the entered data safely stored in a Database
- Get the PDF generated on-the-click of bill generation 
- Add the Inward Stock to the database
- Check the existing stock of any Item in one click
- Check all the details of any Item in one click

## Features

- Easy to choose, categorical arrangements of Items 
- Easy to operate cart-related operations
- Get the entire Input data saved on-a-single-click
- Get the PDF generated for the prepared bill
- Easy Stock Inward module
- Requires no any experience to use
- And some more, to be embedded later on...

## Tech

This Billing Module uses following tools, technologies and open-source project/package to get in the way it is:

- [Python](https://www.python.org/) - for the entire programming and working
- [PyQt5 Package](https://pypi.org/project/PyQt5/) - for designing and developing the intercative and working User Interface
- [SQLite](https://www.sqlite.org/index.html) - for managing all the entered and availabe data into Database
- [Qt Designer](https://www.qt.io/download) - for creating the User Interface easily
- [FPDF](https://pyfpdf.readthedocs.io/en/latest/) - for making the PDF file of the bill invoice made
- Several Python packages like - sqlite3, os, datetime for effective and fruitful working

And of course, with lots of coding and logic of working

## Future Updates

There are several updations on which the work is been carried out, such as:

- Making more optimized software
- Designing a similiar Web App
- Admin-Employee architecture for full fledged working
- Sending Bill and some other notifications on SMS/E-mail
- Updating the existing functionalities

Beside this, There is the scope of much more endeavours to befitted in.

## Installation

It majorly requires [Python](https://www.python.org/) v3+ to run. Make sure the path is added in Environment variables list.
It will also require [SQLite](https://www.sqlite.org/download.html) Database management software for handling all the data operations.
Install all the other dependencies i.e the used packages/libraries:

installing PyQt5 -
```sh
pip install PyQt5
#or you can also use
py -m pip install PyQt5
```

installing SQLite3
```sh
pip install db-sqlite3
#or you can also use
py -m pip install db-sqlite3
```

installing FPDF 
```sh
pip install fpdf
#or you can also use
py -m pip install fpdf
```
(All the above mentioned commands are presented here with respect to the Command Prompt/ Powershell of Windows operating system. they might differ for Terminal of Linux or any other operating system.)

## Standard operating Procedure

### Billing Module:
1. After successfull installation of the mentioned softwares and all other dependencies, one can simply run the python file ( _main.py_ or directly open _bill.py_). An interactive user interface will show up on successful initiation.
2. The user need to enter a unique and appropriate **Invoice Number**. IT IS MANDATORY TO ENTER APPROPRIATE INVOICE NUMBER EVERYTIME. For instance, let the entered value is "101", then after filling all the details, when the "_**GENERATE BILL**_" button will be clicked; the invoice number will get modified as "_currentdate/101_". So, it'll be the final value of Invoice Number. 
The **Date** and **Time** fields will get the deafult set value.
3. Then one need to enter the values for **Customer Name**, **Customer Contact**.
4. After that, one needs to select the **Item Category**. Only after selecting the apt category, the **Item Name** will get displayed into its corresponding dropdown.
5. It is quintessential to mention the **Quantity** of the selected item. Now one can add this into the cart by simply clicking **ADD TO CART**, and can remove the last added entry by clicking **REMOVE**. To reset the Item Name and Quantity field, one needs to click **CLEAR**.
6. After taking all the desired items into the Cart, the user also needs to mention whether any Discount is given or not, by selecting the available allowance from dropdown field of **Discount Percent**. 
7. Then one needs to mention the **Remarks**, if there are any. Along with this, one needs to select the applicable Terms and Condition on the entire purchase, by selecting the one from **T&C** dropdown.
(If "*other*" is selected from the **T&C** dropdown then it is mandatory to mention the proper justification in **Remarks** field)
8. Lastly, the one himself/herself have to mention his/her name, who is the user of this module and entered every data to issue the Bill Invoice in the **Issued By** field.
9. When the **TOTAL** button will get clicked, it will show the total amount to pay for all items, as well as the discount given and based on these, it will finally give the Total Payable Price for entire purchase.
10. On clicking the **Generate Bill** button, all the entered data will get stored into the Database, and at the same time a PDF will get generated that will be viewing on screen to get printed.
11. One can access the database named "*store*" for all data related queries and operations, which is there inside the database folder.

### Stock Registry Module:
1. This module is for registering the Inward Stock and to enter it's details in a database.
2. The user need to enter a unique and appropriate **Invoice Number**. IT IS MANDATORY TO ENTER APPROPRIATE INVOICE NUMBER EVERYTIME. For instance, let the entered value is "101", then after filling all the details, when the "_**ADD TO DATABASE**_" button will be clicked; the invoice number will get modified as "_currentdate/101_". So, it'll be the final value of Invoice Number. 
The **Date** and **Time** fields will get the deafult set value.
3. Then one need to enter the values for **Supplier Name**, **Supplier Contact**.
4. After that, one needs to enter the unique **Item ID** for the product, as well as need to select the **Item Category**; or can also mention **Custom Item Category**, by leaving the **Item Category Selection dropdown** *empty*. After entering the apt category, one will need to enter **Item Name**. This entire step is *mandatory* to perform.
5. It is also required to mention the **Quantity** of the entered item. And then needs to mention clearly about the Price of a sinle unit/item/article in **Price of 1** Input box. Followed by this, one needs to enter the **Total payed amount** that was paid for the entire entry.
6. Then one needs to write down the **Remarks**, if there are any. Along with this, one needs to mention the applicable Terms and Condition on the entire input entry, by typing the one in **T&C** dropdown.
7. Lastly, the one himself/herself have to mention his/her name, who is the user of this module and entered every data in the **Issued By** field.
8. After this, one can also fill the details regarding **Courier Service Name**, **Courier Service Contact** and **Courier Service Reference bill No.**
9. After successfully entering all the inputs, when the **ADD TO DATABASE** button will get clicked, it will store it into *"raw_inventory"* table of *store.db* database.
10. On clicking the **RESET ALL** button, all the entered data will be reset.
11. One can access the database named "*store*" for all data related queries and operations, which is there inside the database folder.

### Stock Checking Module:
1. This module is for checking the current stock availability of any item, as well as to retrieve all the information of any particular item from database.
2. for checking the stock, one firstly need to EITHER select the **Item ID** OR to select the one by selecting proper **Item Category** and **Item Name**.(If one has selected both, then make sure it points to the same item i.e both is for a same product)
3. On clicking **CHECK NOW** button, it will retrieve the present stock of that entered item and display it. 
4. Another function available here is the Information retreival of desired product. For that one firstly need to EITHER select the **Item ID** OR to select the one by selecting proper **Item Category** and **Item Name**.(If one has selected both, then make sure it points to the same item i.e both is for a same product)
5. On clicking **CHECK NOW** button, it will retrieve all the information available in the database; of that entered item and display it. 
6. **CLEAR OUTPUT** button present in both the function is for clearing out the output.


## "Bonus Point"
You can modify it as per your choice, need and requirement, and can also convert the entire project as an executable application. Follow the below mentioned points to do the same:
- install the _pyinstaller_ library:
    ```sh
    pip install pyinstaller
    #or you can also use
    py -m pip install pyinstaller
    ```
- Design a decent looking, creative icon for your .exe application. Make sure it is in _.ico_ format
- Place the _pyinstaller_, _<your icon>.ico_, _<your_python_file>.py_ etc. in a same directory.
- Open the Powershell/Command Prompt/Terminal at the same location i.e above stated directory
- Run the following command:
    ```sh
    pyinstaller -w -F -i "<path of icon file>" <name_of_python_file>
    ```
- It will take some moments to completely perform the operation. On successful completion, it will generate files named as _pycache_, _dist_, _build_ and _<name_of_python_file>.spec_
- You can find your executable application file in _dist_ directory


> Note: `the project is primitive, and might have some flaws; but with upcoming iterations of development, it will surely get uplifted in terms of operations, performance and fruitfulness...` 

Anyone who is keen to work on this, is heartily welcomed.


**Yeah Python... Cheers to the new world !**
