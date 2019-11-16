# Data Engineering
## Roles and Permissions
There are 3 different primitive roles.

* Reader - can only view a GCP project. Cannot change state of anything within the project
* Editor - All of the viewer permissions, plus permissions that allow the change of state. Such as changing existing resources
* Owner - All editor permissions, plus:

    * Permission to add or delete user roles
    * Setup billing for the project

## APIs and Services

Most Cloud APIs provide you with detailed information on your project’s usage of that API, including traffic levels, error rates, and even latencies, helping you to quickly triage problems with applications that use Google services. You can view this information by opening the navigation menu and clicking on APIs & Services > Library:

## Cloud Shell
Now that you understand the key features of GCP and the console, you will get hands-on practice with Cloud Shell. Cloud Shell is an in-browser command prompt execution environment that allows you to enter commands at a terminal prompt to manage resources and services in your GCP project.

Cloud Shell lets you run all of your shell commands without leaving the console and comes with pre-installed command line tools.

Besides pre-installed toolkits, Cloud Shell also comes with the standard unix command line interface (CLI) tools and text editors like nano. We can use these to create and edit files right inside Cloud Shell.