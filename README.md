# Week 10 Lab

Clone this repo into your www folder under laragon. In the command prompt, cd into the \laragon\www folder. Make sure that you are in the correct folder and that laragon\www appears in the command prompt. Type git clone your-repo-url (Get your repo url from github after creating the repo). Then cd into the folder you have just cloned by typing cd week10Lab-yourgithubid. Once you are in the correct folder, keep this command window open so you can type in your git commands as required.

This lab is designed as an introduction to using Sessions and Session Variables. The example is for a simplified airline reservation which will gather data over a number of steps/PHP pages, store the data in session variables and complete an airline reservation.

This assignment has the following objectives
- To ensure students can start a session
- To ensure students can assign values to session variables
- To ensure students can redirect the browser using a PHP instruction
- To retrieve session variables on subsequent pages

# Part 1

Write a PHP program called processForm1.php that when the flightBooking.html form has been submitted, will start a session, gather all the data from the flightBooking.html form, and store it in session variables. The passenger's firstname should be stored in a session variable called $_SESSION['passengerFN'] and the surname should be stored in $_SESSION['passengerSN']. If the luggage checkbox is checked a variable called $_SESSION['luggage'] should be set to 1, if it is unchecked it should be set to 0. ***Note - to use the checkbox input tag from the form you must use the isset() function to verify if the checkbox has been checked***.

If the "Do you want to check luggage" checkbox is checked, the form should re-direct the browswer to the form luggage.html to gather the luggage information. If the luggage checkbox is not checked the program should redirect to the finalStep.php page. 

# Part 2

Write a PHP program called processForm2.php that will be executed when the luggage.html submits to it. This program should gather the number of bags that weigh 10KG or less that the passenger intends bring and the number of bags that weigh between 10 and 20KG. The program should gather the number of under-ten-kilo bags and assign it to a variable called $_SESSION['subTenKG'] and the number of ten-to-twenty-kilo bags and assign it to a session variable called $_SESSION['overTenKG']. After storing the information in session variables the program should redirect the browser to the page finalStep.php. ***Note - the final step is a PHP page as opposed to html, this is because it needs to execute PHP instructions along with html.***

# Part 3

Modify the program finalStep.php so that it outputs the data stored in the session variables which was recorded from the flightBooking.html and luggage.html forms. This program should list out the passenger's firstname, surname and luggage details and ask the user to confirm the details are correct. Make the necessary adjustments to the program so that it echoes the values contained in various session variables. Make sure that an if statement checks that the $_SESSION['luggage'] session variable is set before attempting to output the session variables relating to luggage, if you don't do this there will **UNDEFINED INDEX** errors in relation to those variables. If the confirm checkbox is checked the program should redirect the browser to the confirm.php page.

# Part 4

Create the database for flightBookings stored in the sql file in the repo. If Parts 1, 2, and 3 have been completed correctly the data from the session variables should be inserted into the DB when the confirm checkbox is checked and the submit button is clicked. ***Verify that the credentials in dbcon.php are correct and align with the database setup you are using (this file uses PORT 3307)***



