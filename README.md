# Gmail_to_Excel_keyword_sender_list (1).ipynb

This code searches a Gmail inbox for a specified keyword in the body of the latest specified number of emails. It then extracts unique email senders of emails that contain the specified keyword and stores them in a Pandas DataFrame which is exported to an Excel file. The user is prompted to enter their email address, app password, keyword to search, and number of emails to search through. The program then logs in to the specified Gmail account using the provided credentials, selects the inbox folder, and retrieves the latest specified number of email messages from the inbox. For each email, it parses the email message and extracts the sender's email address. If the email body contains the specified keyword, the email address is added to a set of unique senders. Finally, the set of unique sender email addresses is converted into a Pandas DataFrame which is exported to an Excel file.


## Setup

Before you can run the script, make sure you have installed the following libraries that Python uses to interact with email servers:
`email`,
`imaplib` and
`re`. 


what is an app password for gmail and how do i get it? 
(please note, the App password used in the code was once the correct App password, used to demonstrate what the output of the code will look like. It is no longer the App password to email account '5291ccc@gmail,' so using them in combination will return an authenication error. Please use your own email adress and App password)


An app password is a unique password that allows you to access your Gmail account from third-party apps that do not support two-factor authentication. 
This is to ensure the security of your account while still allowing you to use those apps.
To get an app password for Gmail, you need to follow these steps:

1. Go to your Google Account settings by visiting https://myaccount.google.com/ and sign in if necessary.

2. Click on the "Security" tab on the left-hand side of the page.

3. Under the "Signing in to Google" section, click on "App passwords."

4. You may be asked to enter your Google account password again for security reasons. 
After you enter your password, you will be taken to the app passwords page.

5. Select the app for which you want to generate an app password. (or select 'other' and name the App 'pyscript' - or anything

6. Follow the on-screen instructions to generate the app password. 
You may need to provide the app name, device type, and other details to generate the password.

7. Once the app password is generated, copy it and use it to sign in to the app.

The program should run in less than a minute assuming you are not purposely trying to break it. 

I used this program to find out that The keyword "review" appears 231 time(s) in the body of the latest 150 email messages.
which is ludacris, annoying and i hate when vendors solict reviews from me.

## sender_emails.xlsx
This is the file created by the program. An exmaple file can be found beneath the actual code. The EXCEL file is stored in the same place where the program is stored. Check your file folder on the left side of where you ran the program. Then click the file, download it, and open it in EXCEL

## Why do this when you can use the search bar in gmail? 
I am also building off this program to create a software product that detects if a non-FBA vendor is soliciting reviews from customers via Email (in reward for $25 gift cards) 
these vendors are in violation of the Amazon Terms of Service and solicting reviews  makes for a less transparent, less diverse
and more monopolized market place.


doing it like this allows me to set constraints on how many emails I want to check. This is important for rerunning the program multiple times over the course of some time, to see if an keyword instance still exists, allowing for the creation of a list of vendor email accounts who continue to solict reviews


