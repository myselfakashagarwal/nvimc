![nvim](https://github.com/myselfakashagarwal/nvimc/assets/106314226/bf6ce77f-a794-41a6-9ef3-d67d0de234b7)

Isolated dev-code workspace in terminal preloaded with neovim and cool IDE configurations, all handled by nvimc utility.

![Screenshot 2024-02-05 at 12 56 03 AM](https://github.com/myselfakashagarwal/nvimc/assets/106314226/22b1b1d9-8376-468d-897e-c17ed9328ff4)


### Setup 
Just run the commands below; This will ensure that non privileged user have access to docker becasue the setup depends on spawnning containers via docker also it downloades the utility and stored at the correct placce by itself !. It is to be believed that system has docker awk grep wget. Enjoy !!! 

```bash
sudo wget -O /usr/local/bin/nvimc https://github.com/myselfakashagarwal/nvimc/raw/legacy/nvimc; sudo chmod +x /usr/local/bin/nvimc; sudo groupadd docker 2> /dev/null; sudo gpasswd --add "$USER" docker 2> /dev/null
```

### Command - Usage 

```bash

  Usage: 
  nvimc                          Open the current working directory in the neovim 
  nvimc [OPTIONS] [ARGUMENTS]    Open the neovim with respect to arguments provided

  Options                 Argument                      Action 
  --version , -v          <none>                        To get the current version
  --configure , -c        <none>                        To configure workspace
  --file , -f             <FOLDER>                      To open the provided folder in coder container  
```

### Editor - tutorial 

```text
* Must run in command mode

Editor
i                    Writing mode 
escape+:+wa          Save changes
escape+u             Undo
selection+y          copy stuff
selection+x          cut stuff
ctrl+p               paste stuff

Theme
escape+space+th      Select the desired theme and its all good

Neovim tree
escape+ctrl+n        Open the directory structure aka neovin tree
                     Press 'enter' on file to open it 
                     Press 'a' to add a file
                     press 'r' to rename a file
                     Press 'd' to delete a file

Terminal
sapce+h             Open horizontal terminal in the workspace
space+v             Open vertical terminal in the workspace
                    After its been spawned move the cursor in terminal and press 'i' and insert commands a per need type 'exit' to close the terminal

Editor
escape+:+wq!       To overwrite and exit works for tree and editor, for terminal type command 'exit'
escape+wq          To write adn exit
escape+q!          To exit without saving any changes
```
