# Nice Raspberry Pi conky script 

This is based upon Botspots fork of Novasprit's conky script. 
Personally I like a smaller conky script therefore I edited Botspot's script;
so I made this version of it.

![screenshot](https://github.com/CleanMachine1/piconky/blob/main/conky.png?raw=true)


As you can see, it hasn't got a lot of infomation however it has as much as I feel is required.
## Process To Install:

Open a terminal and type:
` sudo apt install conky && wget -O ~/.conkyrc https://raw.githubusercontent.com/CleanMachine1/piconky/main/conkyscript`

## Optional:


You may want to consider having conky start at startup.
To do this we are going to use cron.
Open a terminal and type:
`crontab -e`

Now, whilst inside of the crontab config enter this line at the bottom:
`@reboot sleep 30 && conky`

Then upon next reboot, 30 seconds should pass then conky should appear. 
NOTE: Please leave the sleep to 30 otherwise it may not appear as crontab launches before desktop meaning it may never show if set to anything lower.

## Process to Uninstall: 
Open terminal and type:
`sudo apt purge conky && rm ~/.conkyrc`

If you did the additional step about autostarting it then run these commands:
`crontab -e` 
and then remove the following line: 
`@reboot sleep 30 && conky`

## Final Notes

If you find anything wrong with my configs, please let me know in the issues section!

