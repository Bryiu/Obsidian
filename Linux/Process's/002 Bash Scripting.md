##### Tutorial Link
https://linuxconfig.org/bash-scripting-tutorial
# Creating a Bash Script
To figure out where the bash interpreter is located

> `which bash`
> /bin/bash

## Make the script

>`nano gaming.sh`

>#!/bin/bash
echo "Starting Steam"
steam &
echo "Starting Spotify"
spotify &
echo "Starting Discord"
discord &
echo "Starting Trading View"
tradingview

## Make the script executable

>`chmod +x gaming.sh`

## Running the Script
>`./gaming.sh`

# Giving the Script an Alias
To make the alias persistent you have to append the .bashrc file.
>nano .bashrc

then: 

>`alias alias_name="command_to_run"`

to make the command available during the current session 

>source ~/.bashrc

# Bash Scripts
[[bills.sh]]
[[programming.sh]]
[[gaming.sh]]
