# README

# Cookiecutter

You will need to install cookiecutter with the [guide](https://cookiecutter.readthedocs.io/en/1.7.2/installation.html)

```
cookiecutter https://github.com/Freedom89/vs-docker-py-dbt
```

You will need to enter 6 inputs:

```
{
	"directory_name":"enter your desired folder name",
	"gcp_project_id":"enter default gcp project",
	"gcp_dataset":"enter default gcp dataset",
	"dbt_folder":"{{cookiecutter.gcp_dataset}}",
	"dbt_project":"{{cookiecutter.gcp_dataset}}",
	"dbt_profile":"Enter your desired dbt profile",
	"_copy_without_render":["*.html","*.scss","*.sql"]
}
```

to specify with env defaults, you can do this: 

```
cookiecutter https://github.com/Freedom89/vs-docker-py-dbt gcp_project_id=$(gcloud config get-value project)
```

# directory_name

Enter the name of the folder you need

# gcp_project_id

The name of your gcp project id where you have access to

# gcp_dataset

Which gcp data set to write to

# dbt_project

[About DBT project](https://docs.getdbt.com/docs/building-a-dbt-project/projects/)

Note, the name of your dbt project does not really matter much. 

Even in the docs: `What should i name my dbt project`:

> The name of your company (in kebab_case) often makes for a good project name.

# dbt_profile

[About DBT profiles](https://docs.getdbt.com/dbt-cli/configure-your-profile/).

This does not matter as much for now until you need to enter multi profiles. 

Future to do:

- add cloudbuild
- add cloudscheduler
- add pydash
- add cli 
- add github pages


