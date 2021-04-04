


# Challenge2 Fintech Bootcamp 

* Improving usability of Loan Qualifier for users

> "After successfully developing The Loan Qualifier application, we decided to improve usability for not-so-technical users. 
With this new improvement software can prompt the user to save the qualifying loans as a new CSV file.
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
[For more information on libryries click on this link]( https://docs.python.org/3/library/csv.html?highlight=csv#module-csv ) 

---

## Installation Guide

In this section, you should include detailed installation notes containing code blocks and screenshots.

To make sure all of the pieces of my modular application is working, you should pull all of the files from Challenge2 repo. 
Chellenge repository was initialized with starter code using Terminal. Same way you can pull it to your computer to create a local repo.

```
git clone https://github.com/nataliaburrey/Challenge2.git

```
You can download Anaconda packedge on MacOC [HERE](https://www.anaconda.com/products/individual)
Make sure to use following packedge:

[
![anaconda_python37](https://user-images.githubusercontent.com/80833988/113497395-828b6980-94b8-11eb-918c-df4a446f817d.png)
](url)

---

## Example: running original Loan Qualifier Application

 Original Loan Qualifier application was asking user to give a path to a CSV file (daily rate sheet), containing a list of the banks and related information to them, such as Lender,Max Loan Amount,Max LTV,Max DTI,Min Credit Score,Interest Rate. 

[
<img width="815" alt="firstQ" src="https://user-images.githubusercontent.com/80833988/113492324-73da8d80-948b-11eb-859f-72fe3938aee7.png">
](url)

If giving the wrong path, the message occurs:
 ```
 
 Oops! Can't find this path
 
 ```
 If the right path given, it promts user dialog to get the applicant's financial information, than calculates users debt-to-income ratio, loan-to-value ratio and filters it through a list of avaliable loans, gives a number of banks ready to give the loan
 
 
[
<img width="540" alt="Screen Shot 2021-04-03 at 2 38 09 PM" src="https://user-images.githubusercontent.com/80833988/113492257-0af31580-948b-11eb-9d6e-a21869a71150.png">
](url)

---

## How to use my project

My project is built on top of Loan Qualifier. Using Loan Qualifier CLI, the tool prompet me to save the results, as a yes/no question so user can opt out of this feature.

[
<img width="818" alt="Screen Shot 2021-04-03 at 3 21 27 PM" src="https://user-images.githubusercontent.com/80833988/113498334-ddc15a00-94c0-11eb-9464-c7cfcd427f8c.png">
](url)

If user chooses to save qualifying loans as a new CSV file, she can find it next to daily_rate_sheet.csv at the following path

```
./data/test.csv 
```

If there would be no qualifying loans, the user will get the following message: 

```
"Sorry, you are not qualified for a loan."

```
and exit. 


## Development and Testing

Chellenge2 local repository was initialized with starter code using Terminal. Changes was pushed to remote repository using  command line

```
git add .
git commit -m "Original commit"
git push
```
Further changes was made by uploading files directly usin GitHub interface.

READme.md was further edited directly on Git Hub to make it easier to preview changes and upload images.

New test was written to make sure new function is working

```
def test_save_csv():
    qualifying_loans = "test"
    csvoutpath = Path("./data/test.csv")
    assert csvoutpath.exists()
```
[
<img width="597" alt="Screen Shot 2021-04-03 at 3 41 19 PM" src="https://user-images.githubusercontent.com/80833988/113498397-68a25480-94c1-11eb-8118-94667c704eb5.png">
](url)


---

# Contributors 

The project was created in collaboration with Berkeley Fintech Bootcamp team : 
Allan Hall, Joel Gonzales, Siege.
AskBCS Learning Assistant was used to troubleshoot some of the accuring problems outside of the classroom
Tutor Lavina Tang helped me to polish my code and tought me how to run separate parts of code to see if it works every step.

Feel free to contact me via channels

* Email:(nataliaburrey@gmail.com) 
[LinkedIn:] (https://www.linkedin.com/in/natalia-burrey-181822175/)
[Instagram:] (https://www.instagram.com/natamclaren/)


---

* License

MIT


