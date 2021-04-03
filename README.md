


# Challenge2 Fintech Bootcamp 

* Inmproving usability of Loan Qualifier for users

> "After successfully developing The Loan Qualifier application, I decided to improve usability for not-so-technical users. 
With this new improvement my software can prompt the user to save the qualifying loans as a new CSV file.
"




---

# Technologies 

The progect was written in Python, using Visual Studio Code to modified the original file. 
I used Terminal on MacOC to run the code and later to create repository,upload and modified files on GitHub. 
Conda (dev) inviroment was activated. Multiple libriries was called to use by following commands:

``` 
import cvs
import sys
import fire
import questionary
from pathlib import Path 
```
[For more information on libryries click on this link:]( https://docs.python.org/3/library/csv.html?highlight=csv#module-csv ) 

---

## Installation Guide

In this section, you should include detailed installation notes containing code blocks and screenshots.

---

## Example: running original Loan Qualifier Application

 Original Loan Qualifier application was asking user to give a path to a CSV file with a list of loans containing list of parameters (daily rate sheet), containing a list of the banks and related information to them, such as Lender,Max Loan Amount,Max LTV,Max DTI,Min Credit Score,Interest Rate. 

[
<img width="815" alt="firstQ" src="https://user-images.githubusercontent.com/80833988/113492324-73da8d80-948b-11eb-859f-72fe3938aee7.png">
](url)

If giving the wrong path, the message occurs:
 ```
 
 Oops! Can't find this path
 
 ```
 if the right path given, it promts user dialog to get the applicant's financial information
 
 ```
 credit_score = questionary.text("What's your credit score?").ask()
    debt = questionary.text("What's your current amount of monthly debt?").ask()
    income = questionary.text("What's your total monthly income?").ask()
    loan_amount = questionary.text("What's your desired loan amount?").ask()
    home_value = questionary.text("What's your home value?").ask()

    credit_score = int(credit_score)
    debt = float(debt)
    income = float(income)
    loan_amount = float(loan_amount)
    home_value = float(home_value)

    return credit_score, debt, income, loan_amount, home_valu
```
 The application than calculates users debt-to-income ratio, loan-to-value ratio and filters it through a list of avaliable loans, gives a number of such
 
 ```
  monthly_debt_ratio = calculate_monthly_debt_ratio(debt, income)
    print(f"The monthly debt to income ratio is {monthly_debt_ratio:.02f}")

    # Calculate loan to value ratio
    loan_to_value_ratio = calculate_loan_to_value_ratio(loan, home_value)
    print(f"The loan to value ratio is {loan_to_value_ratio:.02f}.")

    # Run qualification filters
    bank_data_filtered = filter_max_loan_size(loan, bank_data)
    bank_data_filtered = filter_credit_score(credit_score, bank_data_filtered)
    bank_data_filtered = filter_debt_to_income(monthly_debt_ratio, bank_data_filtered)
    bank_data_filtered = filter_loan_to_value(loan_to_value_ratio, bank_data_filtered)

    print(f"Found {len(bank_data_filtered)} qualifying loans")

    return bank_data_filtered
``` 
You can run this code on the Terminal and this will be a result of interaction with the original Loan Qualifier Application



[
<img width="540" alt="Screen Shot 2021-04-03 at 2 38 09 PM" src="https://user-images.githubusercontent.com/80833988/113492257-0af31580-948b-11eb-9d6e-a21869a71150.png">
](url)

---

## How to use my project

This section should include screenshots, code blocks, or animations explaining how to use your project. To make sure all of the pieces of my modular application is working, you should pull all of the files from Challenge2 repo. Chellenge repository was initialized with starter code using Terminal

``` 
git add .
git commit -m "Original commit"
git push
```

Further changes was made by uploading files directly usin GitHub interface.


READme.md was further edited directly on Git Hub to make it easier to preview changes and upload images.

---

# Contributors 

The project was created in collaboration with Berkeley Fintech Bootcamp team : 
Allan Hall, Joel Gonzales, Siege.
AskBCS Learning Assistant was used to troubleshoot some of the accuring problems outside of classroom
Tutor Lavina Tang helped me to polish my code and tought me how to run separate parts of code to see if it works every step.

Feel free to contact me via channels

* Email:(nataliaburrey@gmail.com) 
[LinkedIn:] (https://www.linkedin.com/in/natalia-burrey-181822175/)
[Instagram:] (https://www.instagram.com/natamclaren/)


---

* License

MIT


