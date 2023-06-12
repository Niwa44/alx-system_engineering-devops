0 a script that prints “Hello, World”, followed by a new line to the standard output - print ("Hello Word", end='\n')
1  a script that displays a confused smiley "(Ôo)' - print("Ôo")
4 Display the last 10 lines of /etc/passwd - tail -n 10 /etc/passwd
5 Display the first 10 lines of /etc/passwd - head -n 10 /etc/passwd
6 Write a script that displays the third line of the file iacta - head -3 iacta | tail -1
7 Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line - echo "Best School" >  '\*\\'"Best School"\'\\*$\?\*\*\*\*\*:)'
8 Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it - ls -la > ls_cwd_content
10  Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders. - find . -type f -name "*.js" -delete
11 Write a script that counts the number of directories and sub-directories in the current directory. - find . -type f -print | wc -l
12 Create a script that displays the 10 newest files in the current directory. - ls -lt | head
13 Create a script that takes a list of words as input and prints only words that appear exactly once. - du | sort -nr
14 Display lines containing the pattern “root” from the file /etc/passwd. - grep "root" /etc/passwd
15 Display the number of lines that contain the pattern “bin” in the file /etc/passwd. - grep -c "bin" /etc/passwd
16 Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd. - grep -A 3 "root" /etc/passwd
17 Display all the lines in the file /etc/passwd that do not contain the pattern “bin”. - grep -v "bin" /etc/passwd
18 Display all lines of the file /etc/ssh/sshd_config starting with a letter. - grep "^[[:alpha:]]" /etc/ssh/sshd_config
19 Replace all characters A and c from input to Z and e respectively. - grep "input" | sed 's/A/Z/g; s/c/e/g'
20 Create a script that removes all letters c and C from input. - print(input().replace('c', '').replace('C', ''))
21  Write a script that reverse its input. - print(input()[::-1])
22 Write a script that displays all users and their home directories, sorted by users. - sort -t ':' -k 1,1 /etc/passwd | cut -d ':' -f 1,6
23_When you run this command, it uses the find command to search for empty files and directories in the current directory (.) and its sub-directories.

The options used in the command are as follows:

-type f specifies to search for files.
-empty specifies to find empty files.
-type d specifies to search for directories.
-printf "%P\n" prints only the name of the file or directory (%P) and adds a new line character (\n).
24 When you run this script, it uses the find command to search for regular files (-type f) with a .gif extension (-iname "*.gif") in the current directory and its sub-directories.

The -printf "%f\n" option prints only the base name of the file (%f) without the path, followed by a new line character (\n).

Then, the sed command is used to remove the .gif extension from each file name (s/\.gif$//). This ensures that only the names without the extension are displayed.

Finally, the LC_ALL=C sort -f command is used to sort the file names in a case-insensitive manner (-f), considering byte values. The LC_ALL=C environment variable ensures a consistent sorting order across different locales.

