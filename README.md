


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

## Examples

This section should include screenshots, code blocks, or animations showing how your project works.                      Original Loan Qualifier application, when run, was asking user to give a path to a CSV file with a list of loans containing list of parameters, such as Lender,Max Loan Amount,Max LTV,Max DTI,Min Credit Score,Interest Rate. 
``` 
csvpath = questionary.text("Enter a file path to a rate-sheet (.csv):").ask()
    csvpath = Path(csvpath)
    if not csvpath.exists():
        sys.exit(f"Oops! Can't find this path: {csvpath}")

    return load_csv(csvpath)
```
If giving the wrong path, you would see the the message:
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

---

## Usage

This section should include screenshots, code blocks, or animations explaining how to use your project.

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


