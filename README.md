# Nice Raspberry Pi conky script 

This is based upon Botspots fork of Novasprit's conky script. 
Personally I like a smaller conky script therefore I edited Botspot's script;
so I made this version of it 

![screenshot](https://github.com/CleanMachine1/piconky/blob/main/conky.png?raw=true)


As you can see, it hasn't got a lot of infomation however it has as much as I feel is required 
## Process To Install:

Open a terminal and type:
` sudo apt install conky && wget -O ~/.conkyrc https://raw.githubusercontent.com/CleanMachine1/piconky/main/conkyscript`

## Optional:


You may want to consider having conky start at startup.
To do this we are going to use a systemd file 
Open a terminal and type:
`wget -O ~/Downloads/conky.service https://raw.githubusercontent.com/CleanMachine1/piconky/main/conky.service && 
 sudo mv ~/Downloads/conky.service /etc/systemd/system/conky.service && sudo systemctl enable conky.service`
 

## Process to Uninstall: 
Open terminal and type:
(If you did the optional step, please first type `sudo systemctl disable conky.service && sudo rm /etc/systemd/system/conky.service`

Else just:

`sudo apt purge conky && rm ~/.conkyrc` 
