# Arithmetic Operations 
  - Take me to [Video Tutorial](https://kodekloud.com/topic/arithmetic-operations/)
  
In this section, we will take a look at "Arithmetic Operations"
- There are different methods with which we can perform arithemetic operations

## expr ( **mind the space**)
- For addition
  ```
  $ expr 6 + 3
  ```
- For substraction
  ```
  $ expr 6 - 3
  ```
- For Division
  ```
  $ expr 6 / 3
  ```
- For Multiplication ( must escape the star symbol with a backslash like this cuz star is a reserved 
rejects character in shell )
  ```
  $ expr 6 \* 3
  ```

- These can be used with vairable substitution as well
  ```
  $ A=6
  $ B=3
  $ expr $A + $B
  $ expr $A - $B
  $ expr $A / $B
  $ expr $A \* $B
  ```
  ![expr](../../images/expr.PNG)
  
## Double Parentheses
- Another method for performing arithmetic operations is double parenthesis. (we encapsulate the expression inside a double parenthesis prefixed with a dollar symbol and either assign this operation to a variable or use echo to print it to screen. 
Otherwise, 
Shell will try to execute the 
output of this operation 
and throw an error "not a valid command".
)
  ```
  $ echo $(( A + B ))
  $ echo $(( A-B ))
  $ echo $((A / B))
  $ echo $((A*B))
  ```
  
- You may also programming language C stype manipulations of variables 
  ```
  $ echo $(( ++A ))
  $ echo $(( --A ))
  $ echo $(( A++ ))
  $ echo $(( A-- ))
  
  ![dp](../../images/dp.PNG)
  
## bc
- expr and "double parentheses" only return decimal output, they do not support floating values.
- For this we use another utility called **`bc`**, it referred to as **`Basic Calculator`**.
- It works in an interactive mode and also you can input to another command as well

  ```
  $ A=10
  $ B=3
  $ expr $A / $B
  $ echo $((A/B))
  $ echo $A / $B |bc -l
  ```
  ![bc](../../images/bc.PNG)
