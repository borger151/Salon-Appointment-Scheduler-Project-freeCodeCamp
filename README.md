# Build a Salon Appointment Scheduler

This is one of the required projects to earn your certification. For this project, you will create an interactive Bash program that uses PostgreSQL to track the customers and appointments for your salon.

This course runs in a virtual Linux machine using Gitpod. Follow these instructions to start the course:
1. Create a GitHub account if you don't have one
2. Click the start button below
3. Login to Gitpod with your GitHub account if you aren't already
4. Once the virtual Linux machine is finished loading, start the CodeRoad extension by:
- Clicking the "hamburger" menu near the top left of the VSCode window,
- Going to the "View" menu,
- Clicking on the "Command Palette" option,
- and running the "CodeRoad: Start" command
5. Follow the instructions in CodeRoad to complete the course

## Complete the tasks below
- You should create a database named salon
- You should connect to your database, then create tables named customers, appointments, and services
- Each table should have a primary key column that automatically increments
- Each primary key column should follow the naming convention, table_name_id. For example, the customers table should have a customer_id key. Note that there’s no s at the end of customer
- Your appointments table should have a customer_id foreign key that references the customer_id column from the customers table
- Your appointments table should have a service_id foreign key that references the service_id column from the services table
- Your customers table should have phone that is a VARCHAR and must be unique
- Your customers and services tables should have a name column
- Your appointments table should have a time column that is a VARCHAR
- You should have at least three rows in your services table for the different services you offer, one with a service_id of 1
- You should create a script file named salon.sh in the project folder
- Your script file should have a “shebang” that uses bash when the file is executed (use #! /bin/bash)
- Your script file should have executable permissions
- You should not use the clear command in your script
- You should display a numbered list of the services you offer before the first prompt for input, each with the format #) <service>. For example, 1) cut, where 1 is the service_id
- If you pick a service that doesn't exist, you should be shown the same list of services again
- Your script should prompt users to enter a service_id, phone number, a name if they aren’t already a customer, and a time. You should use read to read these inputs into variables named SERVICE_ID_SELECTED, CUSTOMER_PHONE, CUSTOMER_NAME, and SERVICE_TIME
- If a phone number entered doesn’t exist, you should get the customers name and enter it, and the phone number, into the customers table
- You can create a row in the appointments table by running your script and entering 1, 555-555-5555, Fabio, 10:30 at each request for input if that phone number isn’t in the customers table. The row should have the customer_id for that customer, and the service_id for the service entered
- You can create another row in the appointments table by running your script and entering 2, 555-555-5555, 11am at each request for input if that phone number is already in the customers table. The row should have the customer_id for that customer, and the service_id for the service entered
- After an appointment is successfully added, you should output the message "I have put you down for a service at time, name". For example, if the user chooses cut as the service, 10:30 is entered for the time, and their name is Fabio in the database the output would be I have put you down for a cut at 10:30, Fabio. Make sure your script finishes running after completing any of the tasks above, or else the tests won't pass

Complete both steps below to finish the challenge.

## Step 1: Complete the project

The project runs in a virtual machine, complete the user stories described in there and get all the tests to pass to finish step 1.

Important: After you pass all the project tests, save a dump of your database into a salon.sql file, as well as your salon.sh file, so you can complete step 2. There will be instructions how to do that within the virtual machine.

## Step 2: Submit your code

When you have completed the project, save all the required files into a public repository and submit the URL to it below.

Required files: salon.sql, salon.sh
