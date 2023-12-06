# shell-script-mesh

Shell scripts have several required constructs that tell the shell environment what to do and when to do it. Of course, most scripts are more complex than the above one.

The shell is, after all, a real programming language, complete with variables, control structures, and so forth. No matter how complicated a script gets, it is still just a list of commands executed sequentially.

! -> she-bang
# echo the Hello World
#!/bin/bash

echo "Hello World"

# listing the file 
#!/bin/sh
ls

# numerical expression
#!/bin/bash

var=$((3+9))
echo $var

# managing the inputs 

#!/bin/bash

echo "Enter a numner"
read a

echo "Enter a numner"
read b

var=$((a+b))
echo $var

# finding area of circle 

cho "Enter the radius : "
read r
echo "Area of the Circle is"
echo "3.14 * $r * $r" | bc

## Shell script to calculate gross salary

#!/bin/bash
echo "enter the basic salary:"
read basal
grosal=$( echo "$basal+((40/100)*$basal)+((20/100)*$basal)" | bc -l)
echo "The gross salary : $grosal"

## Creating and Using Variables

#!/bin/bash

millennium_text="Years since the millennium:"

current_time=$( date '+%H:%M:%S' )
todays_date=$( date '+%F' )
year=$( date '+%Y' )

echo "Current time:" $current_time
echo "Today's date:" $todays_date

years_since_Y2K=$(( year - 2000 ))

echo $millennium_text $years_since_Y2K

# script to sleep

#!/bin/bash

echo "Wait for 5 seconds"
sleep 5
echo "Completed"
