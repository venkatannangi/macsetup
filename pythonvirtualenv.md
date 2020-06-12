Instructions 
---------------------
1) install virtualenv using pip3/pip
    ```buildoutcfg
    sudo pip3 install virtualenv
    ```
2) install virtualenvwrapper using pip3/pip
    ```buildoutcfg
   sudo pip3 insatll virtualenvwrapper
    ```
3) Add virtualenv parameters to ~/.zshrc
    ```buildoutcfg
    # set where virutal environments will live
    export WORKON_HOME=$HOME/.virtualenvs
    # ensure all new environments are isolated from the site-packages directory
    export VIRTUALENVWRAPPER_VIRTUALENV_ARGS='--no-site-packages'
    # use the same directory for virtualenvs as virtualenvwrapper
    export PIP_VIRTUALENV_BASE=$WORKON_HOME
    export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python
    # makes pip detect an active virtualenv and install to it
    export PIP_RESPECT_VIRTUALENV=true
    if [[ -r /usr/local/bin/virtualenvwrapper.sh ]]; then
        source /usr/local/bin/virtualenvwrapper.sh
    else
        echo "WARNING: Can't find virtualenvwrapper.sh"
    fi
    ```
 4) Test the deployment by running the below command
    ```buildoutcfg
      mkvirualenv
      workon
    ```