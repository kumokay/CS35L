#!/bin/bash
sed '/<!DOCTYPE/, /Adopt<\/td>/d' |   # delete begin
sed '/<\/table>/, /<\/html>/d' |      # delete end
sed '/<\/tr>/,/<\/td>/d' |            # delete english words
sed 's/<[^>]*>//g' |                  # delete html tags
sed s/\`/\'/g |                       # replace ` with '
tr [:upper:] [:lower:] |              # convert all uppercase letters to lower
sed 's/\,/\n/g'  |                    # replace , with \n to seperate words
sed '/^\s*$/d'   |                    # delete all blanks lines
tr -d [:blank:]  |                    # delete all blanks
tr -cs "pk\'mnwlhaeiou" '[\n*]' |     # delete all entries that contain non-Hawaiian letters
sort -u                               # sort the dictionary, leave only unique entries
~
