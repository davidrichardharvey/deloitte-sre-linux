# Filtering

## Instructions

Branch off from main, and then update this README with the answers / commands used for each question.
Add, commit and push your changes in git, and then submit a pull request on github.
Please put your answers between the `quotes`

## Exercise
1. Use cat, head and tail to output lines 5 through 7 of /etc/passwd with each line preceded with its line number.
    1. ANSWER: `cat -n /etc/passwd | tail -n +5 | head -3`

2. Display all but the first 5 lines of /etc/passwd. Display only the last 20 lines of /etc/passwd, and prove they are.
    1. ANSWER: `cat -n /etc/passwd | tail -n +6;cat -n /etc/passwd | tail -20`

3. Sort only the files in /etc in the following ways (one at a time!).
   * alpha-numerically by file name
      1. ANSWER: `ls -la /etc | awk '$1 !~ /^d|^l/ {print $NF}'`
   * numerically by file size
      1. ANSWER: `ls -laS /etc | awk '$1 !~ /^d|^l/ {print $NF}'`
   * on the second character of the filename.
      1. ANSWER: `ls -laS /etc | awk '$1 !~ /^d|^l/ {print $NF}' | sort -k1.2`

4. Extract the permission bits from the output of ls and display only the permissions. Paste the permissions together so that they appear in 4 columns.
(Ensure that the line containing 'total' is not part of the output!).  You will need to look up the command **paste**
    1. ANSWER: `ls -la /etc | awk '{print $1}' | tail -n +2 | column -c 64`

5. List the files in the /usr/bin directory twice (using one ls command ), and using sort and uniq remove the duplicates.
    1. ANSWER: `ls /usr/bin | sed 'p' | uniq`

6. List the files in /etc, cut the first 4 characters, and use uniq count duplicates.
    1. ANSWER: `ls -la /etc | awk '{print $NF}' | cut -c 5- | sort | uniq`

6. Using man ls, remove all non-word characters and split each word onto a separate line.
From that output you should then work out what the 10 most popular words are in that page.
    1. ANSWER: `man ls | cat | sed "s/\ /\n/g" | sed "/\W/d" | sort | uniq -c | sort -k1nr | tail -n +2 | head`
