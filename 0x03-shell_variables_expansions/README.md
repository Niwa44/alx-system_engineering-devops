Create a script that creates an alias. - alias ls="rm *"
1_ Create a script that prints hello user, where user is the current Linux user. - echo "Hello $USER"
2_dd /action to the PATH. /action should be the last directory the shell looks into when looking for a program.- export PATH="$PATH:/action"
3_Create a script that counts the number of directories in the PATH. - echo "$PATH | wc -l"
4_Create a script that lists environment variables.-  env | sort
5_Create a script that lists all local variables and environment variables, and functions. - set | env 
6_Create a script that creates a new local variable.

Name: BEST
Value: School  command is BEST="School"
7_Create a script that creates a new global variable.

Name: BEST
Value: School - the command is export BEST="School"
8_Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line. - echo $((128 + TRUEKNOWLEDGE))
9_Write a script that prints the result of POWER divided by DIVIDE, followed by a new line.

POWER and DIVIDE are environment variables. the command is echo "scale=2; $POWER / $DIVIDE" | bc
his script uses the echo command to pass an expression to the bc command, which is a calculator for the command line. The scale=2 sets the decimal precision to 2. The expression $POWER / $DIVIDE performs the division, and bc evaluates it. The result is then printed by echo. The newline character is automatically added after the result
10_Write a script that displays the result of BREATH to the power LOVE

BREATH and LOVE are environment variables
The script should display the result, followed by a new line. The command is echo "$BREATH^$LOVE" | bc
11_Write a script that converts a number from base 2 to base 10.

The number in base 2 is stored in the environment variable BINARY
The script should display the number in base 10, followed by a new line. The command is echo "ibase=2; $BINARY" | bc
12_Create a script that prints all possible combinations of two letters, except oo.

Letters are lower cases, from a to z
One combination per line
The output should be alpha ordered, starting with aa
Do not print oo
Your script file should contain maximum 64 characters the command is echo {a..z}{a..z} | tr -s ' ' '\n' | grep -v "oo"
13_Write a script that prints a number with two decimal places, followed by a new line.

The number will be stored in the environment variable NUM. the command is printf "%.2f\n" $NUM
14_Write a script that converts a number from base 10 to base 16.

The number in base 10 is stored in the environment variable DECIMAL
The script should display the number in base 16, followed by a new line. the command is printf "%x\n" $DECIMAL
16_Write a script that prints every other line from the input, starting with the first line. the command is sed -n 'p;n' < input.txt
17_Write a shell script that adds the two numbers stored in the environment variables WATER and STIR and prints the result.

WATER is in base water
STIR is in base stir.
The result should be in base bestchol. the command is echo "ibase=water; obase=bestchol; $WATER + $STIR" | bc


