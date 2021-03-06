202206242058
Tags: #linux  #bash_script

---

# Sed in Linux

sed stands for **Stream Editor**

```bash
# print lines 1,2,3
sed -n '1,3p' sed_test.txt

# print lines that contain 'string'
sed -n '/string/p' sed_test.txt

# print lines that do not contain 'string'
 sed -n '/string/!p' sed_test.txt

sed 's/search-pattern/replacement-string/flags'

# flag i - insetsitive
sed 's/search-pattern/replacement-string/i'

# By default replace first occurrence of the search pattern
# flag g - global
sed 's/my wife/sed/ig' love.txt

# -i - in place editing
sed -i 's/my wife/sed/ig' love.txt

# edit love.txt and create backup file with name love.txt.bak
sed -i.bak 's/my wife/sed/ig' love.txt

# create like.txt and replace love to like in file only with lines, that matched to the pattern
sed 's/love/like/gw like.txt' love.txt

# delelimiter '#'
echo '/home/bulat' | sed 's#/home/bulat#/export/users/bulats#'

# deleting line, that match to pattern
sed '/Second/d' love.txt


# delete lines that begin with '#' and empty lines
sed '/^#/d ; /^$/d' some-conf-file

# execute different types of a commands
sed '/^#/d ; /^$/d ; s/HOST/HOSTNAME/g' some-conf-file

# another way ⬆️
sed -e '/^#/d' -e '/^$/d' -e 's/USER/USERNAME/' some-conf-file

# another way ⬆️
echo '/^#/d' > script.sed  
echo '/^$/d' >> script.sed  
echo 's/USER/USERNAME/' >> script.sed  
sed -f script.sed some-conf-file

# replace only on the second line
sed '2 s/my wife/sed/' love.txt

# replace only on the line, where has 'Group' word
sed '/Group/ s/my wife/sed/' love.txt

# print string(s) that begin with <INSERT home_call.> and end with <);>
sed -n '/^INSERT home_call./,/);$/!p' sed_test.txt

find <mydir> -type f -exec sed -i 's/<string1>/<string2>/g' {} +
```

---
## Links