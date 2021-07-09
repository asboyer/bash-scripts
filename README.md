# Useful bash scripts
### by Andrew Boyer

## Scripts:
* **commit:** will execute `git add .` `git commit -m "message"` and `git push origin master` all at once (useful for quickly updating a repository) 

    > - arg1 = commit message
    > - arg2 = files to add
    > - arg3 = branch name
    > - arg4 = remote name
    > *all arguments are optional*
    
    ### Examples:
    #### Example #1:
    ```shell
    commit
    ```
    executes these commands:
    ```shell
    git add .
    git commit -m "automated commit
    git push origin master
    ``` 

    #### Example #2:
    ```shell
    commit "edited README" README.md
    
    ```
    executes these commands:
    ```shell
    git add README.md
    git commit -m "edited README"
    git push origin master
    ```

    #### Example #3:
    ```shell
    commit "edited main" main.py boyer-dev upstream
    ```
    executes these commands:
    ```shell
    git add main.py
    git commit -m "edited main"
    git push upstream boyer-dev
    ```

* **libclean:** will delete the `dist` `build` and `egg-info` directories made when creating a python package (useful for quickly cleaning up enviroment after creating a python package)
* **update:** will execute `sudo apt update && sudo apt upgrade` (useful for quickly updating and upgrading computer in one command)

## Using these scripts:
* `git clone https://github.com/asboyer2/bash-scripts.git`
* add `/path/to/bash-scripts/bin` to your `$PATH` variable in your `.bashrc
	* **ex:** `export PATH=/usr/root/bash-scripts/bin:$PATH`
* Source your `.bashrc` using the command `. .bashrc`
