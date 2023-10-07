```shell
while read var; do
  var1=$(echo $var | awk '{print $2}')
  var=${var//*123/}
done < file.txt

## sort file and remove same lines
sort file.txt | uniq -c > new.txt

rsync --delete-before -a -H -v --progress -stats ./blank/ ./dir_to_be_deleted/

```
