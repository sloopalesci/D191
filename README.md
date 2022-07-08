# D191
Advanced Data Management 
Here are the requirements of the project

√ The submission accurately and completely summarizes 1 real-world business report created from the chosen dataset.

√ The submission accurately and completely describes the data that will be used in the report.

√ The submission identifies 2 tables from the given dataset that provide the data necessary for the detailed and summary sections of the report.

√ The submission identifies all of the specific fields that will be included in the detailed and summary sections of the report.

√ The submission identifies 1 field in the detailed section of the report that will require a custom transformation and explains why it should be transformed.

√ The submission thoroughly explains the business uses of the summary and the detailed sections of your report and how these sections can be used to improve business

√ The explanation of how frequently the report should be refreshed to remain relevant to stakeholders has a reasonable frequency. The explanation is adequate and logical.

√ The SQL code that creates the tables to hold the report sections is correct and complete.

√ The SQL query provided correctly queries the raw data needed for the Detailed section of the report from the source database and verifies the data’s accuracy.

√ The code for the function(s) that perform the transformation(s) identified in part A4 produced the expected transformations and all previously identified functions are included in the submission.

√ The SQL code successfully creates a trigger on the detailed table of the report that will continually update the summary table as data is added to the detailed table.

√ The stored procedure provided refreshes the data in both the detailed and summary tables, and it can clear the contents of the detailed and summary tables and perform the ETL load process from part C. The submission includes comments that identify how often the stored procedure should be executed.

√ The explanation of how the stored procedure can be run on a schedule to ensure data freshness is accurate and complete

The Panopto video recording includes a full demonstration of the functionality of the code used for the analysis and an accurate and complete summary of the programming environment.

√ The record the web sources used to acquire data or segments of third-party code to support the application is both complete and accurate, and the web sources cited are reliable.Or the candidate did not use any web sources to acquire data or segments of third-party code and stated this in their submission.

√ The submission includes in-text citations for sources that are properly quoted, paraphrased, or summarized and a reference list that accurately identifies the author, date, title, and source location as available

√ Content reflects attention to detail, is organized, and focuses on the main ideas as prescribed in the task or chosen by the candidate. Terminology is pertinent, is used correctly, and effectively conveys the intended meaning. Mechanics, usage, and grammar promote accurate interpretation and understanding.



Write the paper:

A.   Summarize one real-world business report that can be created from the attached Data Sets and Associated Dictionaries. 
We have a new data analyst for Cubebuster Video. There is a new company in town called Internetflix and sales are slipping. The marketing team wants to do some targeted outreach to the customers that are not as active as the rest. They want contact information for the 25 customers that have the least number of rentals for all time. The first campaign is going to be an email blast, so we need a list of full names and emails. If we have that data, we can bulk import it into our email provider. 

1.  Describe the data used for the report.
We're going to be getting contact information from the customers so we'll need:
	First Name
	Last Name
	Number of rentals
	Email
	Full Address
	Phone Number

2.  Identify two or more specific tables from the given dataset that will provide the data necessary for the detailed and the summary sections of the report.
The tables that we'll be working with are:
Rental to determine the number of rentals
Customer to get the first name, last name, and email 
Address to get the address and phone
City to get the city portion of the address

3.  Identify the specific fields that will be included in the detailed and the summary sections of the report. 
The detailed section is going to include:
	customer_id 
	first_name
	last_name
	num_rentals 
	email 
	address 
	address2 
	city 
	postal_code 
	phone 

The summary is just going to be:
	full_name
	email

4.  Identify one field in the detailed section that will require a custom transformation and explain why it should be transformed. For example, you might translate a field with a value of ‘N’ to ‘No’ and ‘Y’ to ‘Yes’.
In order for our email marketing app to accept an import, the email addresses all need to be uppercase. To accomplish this, we'll use the UPPER() function.

5.  Explain the different business uses of the detailed and the summary sections of the report.
The detailed version of the report can be used for any type of marketing since it contains all the contact information. However, as specific marketing campaigns are run, different data is needed for bulk uploading. In this case, the marketing team is doing an email campaign so only the name and email is needed.

6.  Explain how frequently your report should be refreshed to remain relevant to stakeholders.
This report should only need to be run on a quarterly basis. Any more than that and you'll be inviting the customers to hit that 'unsubscribe' button. Additionally, we want to give the campaign time to get to the customer and the customer time to act upon the contents (coupon).

F1. Explain how the stored procedure can be run on a schedule to ensure data freshness.
On the first day of the quarter, the data analyst will have to run the procedure for delivery to the marketing team. To run the procedure, simply query "call create_reports();" in PGAdmin and both reports will be automatically created, ready for export. We don't want to do more than once a quarter because we don't want to spam our low usage customers to frustration. We want to gently remind them that they have our services available.
Footer
© 2022 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
You have no unread notifications
