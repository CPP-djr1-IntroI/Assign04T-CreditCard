## Intro to C++ I

**Assign 04 - Credit Card Processing**

**Date assigned:** 

**Program due:**

**Points:**

**This is an individual assignment.**

**Goals:**

1.  Read and process data from a file

2.  Write C++ code with nested logic

3.  Error check your program using multiple test files

Most people pay a large portion of their bills with a credit card.
Unfortunately, many maintain a balance with a large interest rate. You
are to write a C++ program that processes the credit card account
activity for zero or more individuals. The account activity will be
maintained in a data file called **creditcard.txt** with the following
format.

<pre>
AccountNumber Date Transaction BeginningBalance
AccountNumber Date TransactionLocation TransactionAmount
AccountNumber Date TransactionLocation TransactionAmount
NewAccountNumber Date Transaction BeginningBalance
NewAccountNumber Date TransactionLocation TransactionAmount
...
00000 00/00/00 End 0.0
</pre>

Here is a sample data file:

<pre>
12345 10/01/14 Balance 1500.00
12345 10/01/14 McDonalds 10.75
12345 10/05/14 Walmart 50.65
54321 10/01/14 Balance 16.75
54321 10/06/14 McMenamins 23.00
54321 10/07/14 Payment -25.00
54321 10/10/14 Comcast 130.01
00000 00/00/00 End 0.0
</pre>

In order to process this data file you need to do the following:

1\) Read in the account number, date, transaction, and beginning balance
for an individual. The beginning balance is the unpaid portion from the
previous month

2\) Calculate the interest on the unpaid balance. The interest rate is a
yearly interest rate; however, the interest is calculated using a
monthly interest rate because bills are sent out monthly. If the
previous balance is \<= \$1,000, then the interest rate is 15%;
otherwise, the interest rate is 18.5%.

3\) Process each transaction one line at a time until either the
sentinel value of 00000 is read or a different account is read. Before
beginning to process the next individual, print out summary account
information as shown on the next page.

The solution to this problem could be done with a nested loop, but you
are to use a single loop in your solution. Nested loop solutions will
lose points.

Here is an example of the output after processing the above data file.

<pre>
*********************************
*    Credit Card Processing     *
*********************************

Account: 12345
Previous Balance: $1500.00
Interest Rate: 18.50%

Date        Purchase                Amount
10/01/14    Interest                 23.12
10/01/14    McDonalds                10.75
10/05/14    Walmart                  50.65
            Final Balance          1584.53

Account: 54321
Previous Balance: $16.75
Interest Rate: 15.00%

Date        Purchase                Amount
10/01/14    Interest                  0.21
10/06/14    McMenamins               23.00
10/07/14    Payment                 -25.00
10/10/14    Comcast                 130.01
            Final Balance           144.97

</pre>

**Note**: Date starts in column 1, Purchase starts in column 13, and
Amount starts in column 37. The transaction name will not be longer than
18 characters.

**To complete this assignment you must submit the following:**

1.  **An electronic Solution of your program on GitHub**

    a.  You are to click on the Assign04 Link to accept this
        assignment as we've done in lab. Once accepted, code up a
        complete solution to the above assignment specification. Your
        complete solution is to be pushed to GitHub no later than the
        date and time specified above for your specific section. I will
        only grade your solution from the proper location on GitHub.

    b.  Pay attention to the example output above. Your program's output
        must look **exactly** like the example output! The spacing and
        newlines in your output must match exactly.

    c.  Make sure that your program compiles and runs correctly with no
        errors and no warnings. If you get any errors, double check that
        you typed everything correctly. Be aware that C++ is
        case-sensitive.

2.   **An electronic copy of your program (punetidAssign04CreditCard.pdf) is 
to be emailed to ryandj@pacificu.edu**
