```bash

# Read every line from file
while read var; do
done < file.txt

for i in {1..5}; do
  echo $i
done

for i in 1 2 3 4 5; do
  echo $i
done

for i in `cat file.txt`; do
  echo $i
done

for (( i=0; i<=100; i++ )); do
  echo $i
  if [ $i -eq 2 ]; then
    break
  fi
done

# "$@" is all of the parameters passed to the script
files="$@"
for i in $files; do
  if [ -f $i ]; then
    echo $i " exist"
  fi
done

# Get the second string separated by spaces.
var1=$(echo $var | awk '{print $2}')

# Remove "str1" from a string variable
var=${var//str1/}

# Sort the content based on the second column and remove duplicate lines.
sort －k2,2 file.txt | uniq -c > new.txt

# Replace "str1" with "str2" in the file.
sed -i 's/str1/str2/g' file.txt

# Delete lines containing "str1"
grep -v "str1" file.txt > newfile.txt

# Get lines containing "str1"
grep "str1" file.txt > newfile.txt

# Delete a large folder
rsync --delete-before -a -H -v --progress -stats ./blank/ ./dir_to_be_deleted/
```
