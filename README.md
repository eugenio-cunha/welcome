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