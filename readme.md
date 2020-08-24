# General notes :unlock:


## Job Notes 
----------------

### *Auth and permissions*

You may use Role-based Authorization Strategy pluggin

* Global roles 
* User
* Project roles



### *Custom hooks in Gitlab administered*


Git has a way to fire off custom scripts when certain important actions occur. There are two groups of these hooks: client-side and server-side. Client-side hooks are triggered by operations such as committing and merging, while server-side hooks run on network operations such as receiving pushed commits.



1. Look at  /var/opt/gitlabt/git-data/respositories/{{group}}/{{project}}.git
2. Create the folder *custom_hooks*
3. Go into custom_hooks
4. Create hook (e.g : post or pre-receive )
5. Give permissions chmod 755 post-receive
6. Go back by using cd ..
7. Change the owner of custom_hooks, chown git:git custom_hooks/ -R
   

### *Setting up ENV variables*

By going throught the general setting -> Environment variables.

### *Scheduled builds*

I recomend you to stop by   https://crontab.guru/

Inside the Jenkins jobs, we can find the built triggers option and there we can set *Build periodically*



### *Pipeline*

A pipeline in software development consists of set of tools, flows, and automated processes, enabling teams to leverage technologies to build and deploy software.

1. SCM
2. Build
3. Test
4. Deploy(Prod or Test)
   

## Docker notes  :whale:
----------------

### *Walk into the container by using console*

    docker exec -ti jenkins bash

### *Changing user*

    docker exec -it -u root jenkins /bin/bash


### Copy files 

    docker cp PATH_IN_HOST CONTAINER_NAME:PATH_IN_CONTAINER



# Utils :dart:
----
### *Generate  ssh key*

    ssh-keygen -f name

### *connect with the key* 

    ssh -i key usar@dns
    ssh -i remote-key remote_user@remote_host

