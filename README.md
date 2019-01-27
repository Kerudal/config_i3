# config_i3

# Change your shell : 
In linux it is possible to change the type of shell you're using. Here is the liste of the **5 most frequently used shells for Linux** : 
* Bash 
* Tcsh 
* Ksh 
* Zsh 
* Fish 


To knwo the shell you are using right now just type : 
```bash 
$ echo $0 
```

You can also get the list of shell you have installed with 
```bash 
$ cat /etc/shells
/bin/sh
/bin/bash
/bin/rbash
/bin/dash
/bin/zsh
/usr/bin/zsh
```

In this example i'll be using *zsh shell*. 
To install the shell you need to use **apt install** : 
```bash 
sudo apt install zsh 
```

To change your default shell you need to use : 
```bash
$ chsh --shell /bin/zsh <username>        
```
It will then ask your password. However you need to restart your computer for it to apply the change or exit i3 

To switch between shell, you just need to type : 
```bash 
$ /bin/zsh
$ exit       #goes back to your default 
```

Now you are ready to use zsh, however it is possible to make some personnal configuration by making changes in the file *.zshrc* 


Once you have installed the zsh shell, you should install **Oh my ZSH**. It offers a large variety of theme to install for your terminal : 
```zsh 
cd
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
``` 
You now have to install the powerline font : 
```zsh
cd
wget https://github.com/powerline/powerline/raw/develop/font/PowerlineSymbols.otf
wget https://github.com/powerline/powerline/raw/develop/font/10-powerline-symbols.conf
mkdir ~/.fonts/
mv PowerlineSymbols.otf ~/.fonts/
mkdir -p .config/fontconfig/conf.d #if directory doesn't exists
```
You can clean the cash : 
```zsh 
fc-cache -vf ~/.fonts/
```
Move the configuration file 
```zsh 
mv 10-powerline-symbols.conf ~/.config/fontconfig/conf.d/
```
You may now change the **theme** by opening the file 
```zsh 
nano ~/.zshrc 
```
And in the code you will find **ZSH_THEME="put_the_name_of_the_theme_you_want"**, here is an example : 
```
ZSH_THEME="agnoster"
```
This [website] (https://github.com/robbyrussell/oh-my-zsh)has a list of all the themes you could install on oh my zsh 
