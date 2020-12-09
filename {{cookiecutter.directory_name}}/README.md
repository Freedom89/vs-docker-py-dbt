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

* For your scripts: [[src/README]] 
* For your notebooks: [[notebooks/README]] 

## Env Vars

Edit the env vars you need in your docker image. 

# Save without formatting

In the vscode extensions, it is using [this formatter](https://github.com/henriblancke/vscode-dbt-formatter){target="_blank"} which is using [another formatter](https://github.com/henriblancke/dbt-formatter){target="_blank"} under the hood.


The current sql dialects only support `snowflake` at the moment, as such you might experience weird behavior when using BQ specific functions such as `SAFE_CAST`. 

To overcome this, just [save without formatting](https://code.visualstudio.com/updates/v1_28#_save-without-formatters){target="_blank"}. In summary there are two options:

* `⌘K S`.
* `Cmd+⌘+P` to open user settings and select `File: Save without formatting`.