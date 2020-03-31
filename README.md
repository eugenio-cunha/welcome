# welcome
Cool Custom Welcome Messages on Linux terminal

## Add in .bashrc

```sh
function welcome() {

  text="░██╗░░░░░░░██╗███████╗██╗░░░░░░█████╗░░█████╗░███╗░░░███╗███████╗\n"
  text+="░██║░░██╗░░██║██╔════╝██║░░░░░██╔══██╗██╔══██╗████╗░████║██╔════╝\n"
  text+="░╚██╗████╗██╔╝█████╗░░██║░░░░░██║░░╚═╝██║░░██║██╔████╔██║█████╗░░\n"
  text+="░░████╔═████║░██╔══╝░░██║░░░░░██║░░██╗██║░░██║██║╚██╔╝██║██╔══╝░░\n"
  text+="░░╚██╔╝░╚██╔╝░███████╗███████╗╚█████╔╝╚█████╔╝██║░╚═╝░██║███████╗\n"
  text+="░░░╚═╝░░░╚═╝░░╚══════╝╚══════╝░╚════╝░░╚════╝░╚═╝░░░░░╚═╝╚══════╝\n"
  user_name="$(getent passwd $USER | cut -d ':' -f 5)"
  version="$(uname -mrs)"
  printf "TERMINAL $version\n\n$text\n[Mr. $user_name]>_ Supreme Master of the Universe\n\n";
}

welcome
```
## Sample
![Welcome](https://github.com/eugenio-cunha/welcome/blob/master/terminal.png)

## Change Terminal
```sh
if [ "$color_prompt" = yes ]; then
    PS1='[${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\]\[\033[01;34m\] \W\[\033[00m\]]>'
else
    PS1='[${debian_chroot:+($debian_chroot)}\u@\h \W]>'
fi

```
