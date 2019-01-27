# config_i3

# Change your shell : 
In linux it is possible to change the type of shell you're using. Here is the liste of the **5 most frequently used shells for Linux** : 
* Bash 
* Tcsh 
* Ksh 
* Zsh 
* Fish 


To knwo the shell you are using right know just type : 
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

In this example i'll be using *Zsh Shell*. 

To change your default shell you need to use : 
```bash
chsh --shell /bin/zsh usernam  
```
It will then ask your password 
However i think you need to restar your computer for it to apply 

And to switch between shell, you just need to type : 
```bash 
/bin/zsh
```


