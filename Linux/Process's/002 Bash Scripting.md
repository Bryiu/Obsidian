##### [Tutorial Link](https://linuxconfig.org/bash-scripting-tutorial)

# Creating a Bash Script
To figure out where the bash interpreter is located

```bash
which bash

/bin/bash
```
## Make the script

```bash
nano gaming.sh
```

```bash
#!/bin/bash
echo "Starting Steam"
steam &
echo "Starting Spotify"
spotify &
echo "Starting Discord"
discord &
echo "Starting Trading View"
tradingview
```
## Make the script executable

```bash
chmod +x gaming.sh
```

## Running the Script
```bash
./gaming.sh
```

# Giving the Script an Alias
To make the alias persistent you have to append the .bashrc file.
```bash
nano .bashrc
```

then: 

```bash
alias alias_name="command_to_run"
```

to make the command available during the current session 

```bash
source ~/.bashrc
```

# Bash Scripts
[[bills.sh]]
[[programming.sh]]
[[gaming.sh]]

# Examples
## Bash Script with [[Bash Commands]]
```bash
#!/bin/bash

name=$1
compliment=$2

user=$(whoami)
date=$(date)
whereami=$(pwd)

echo "Good Morning $name!"
sleep 1
echo "You're looking good today $name!"
sleep 1
echo "You have the best $compliment I've ever seen $name!"
sleep 2
echo "You are currently logged in as $user and you are in the directory $whereami. Also today is: $date"
```

### Explaination
After the shebang is the variables. These first two variables take in the inputs of arguments passed into the terminal after the bash script is ran in order. 

The second variables take in the outputs of the bash commands. So user becomes the $whoami output. 

[Here](obsidian://open?vault=Obsidian&file=Linux%2FBash%20Commands) is a list of bash commands
