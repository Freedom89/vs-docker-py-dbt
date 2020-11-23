# main

This docker image is build on top of [vscode remote container development.](https://code.visualstudio.com/docs/remote/containers) 

The default dbt database is bigquery. 

# Launch in vscode

* Install the recommended extensions
* Open command palette
* Select `remote-containers reubild and reopen in container` option. 
	* Select from `Dockerfile` 

# Pre-Req

* Understanding of docker
* Understanding of [dbt](https://docs.getdbt.com/) 

## foam

This links are populated with [foam](https://foambubble.github.io/foam/).

## dbt

Look at [[dbt/README]] on how to use dbt. 

## Using python

For your scripts: [[src/README]] 
For your notebooks: [[notebooks/README]] 

# Env Vars

Edit the env vars you need in your docker image. 
