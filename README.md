Download link :https://programmingsolver.com/questions-and-answers/div-c-implementing-integer-division-using-bitwise-operators-in-c/

Files to submit: div.c

Time it took Matthew to complete: 10 mins

Write a C program called div.c that implements division on two unsigned integers.

Name your executable div.out

You cannot use division in your solution

Arguments should be accepted from the command line

The first argument is the dividend

The second argument is divisor

Your program should display the quotient and remainder after doing the division

Your program must complete in O(1) (constant) time

This is possible because an integer is 32 bits long and so the loop that does the division should not take longer than 32 iterations.

Because of this restriction the following solution is not acceptable as it does not meet the O requirements

void bad_div(unsigned int dividend, unsigned int divisor,

unsigned int* quotient, unsigned int *remainder){

*quotient = 0;

while(dividend >= divisor){

(*quotient)++;

dividend -= divisor;

}

*remainder = dividend;

}

In order to meet the O requirements you will have to division in base 2 as you would by hand. See these 2 articles for some examples: Dr. Math and Exploring Binary

Hint: use bitwise operators

The one step that they leave out and one that you normally skip when doing division by hand is checking to see how many times the divisor goes into the dividend for the numbers that contain fewer digits than the divisor.

For example: 30 / 15

First we should check how many times does 15 go into 3. The answer is 0.

Then we check how many times does 15 go into 30, which is 2.

So our answer would be 02 R 0

Examples:

./div.out 10 5

/5=2R0

2. ./div.out 100 17

100/17=5R15

加QQ codinghelp Email: programminghelp1@proton.me

