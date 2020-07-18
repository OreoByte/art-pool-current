# Basic guide to color and change your ASCII art with "tput xterm" and PS1 Shell

# Set text color "foreground" with setaf
	echo "$(tput -T xterm setaf 'color_number')"
	echo "$(tput -T xterm setaf 2)"

# Set background color with setab
	echo "$(tput -T xterm setab 'color_number')"
	echo "$(tput -T xterm setab 6)" 

# The basic 8 color options for tput
        0 = black
        1 = red
        2 = green
        3 = yellow
        4 = blue
        5 = magenta
        6 = cyan
        7 = white
        
# PS1 Shell to underline ASCII chars 
	printf "\e[4m"

# PS1 Shell for Bold text / ASCII 
	printf "\e[1m"

# For both Bold and underlined option on one line
	printf "\e[1m\e[4m"

# Example Linux bash script "bold, underline, and color cyan"
	Add printf "\n" (newline) if needed

	#!/bin/bash

	printf "\e[1m\e[4m"

	echo "$(tput -T xterm setaf 6)"

	printf "\n"

	cat /your/path/to/ascii_art.txt

	printf "\n"
