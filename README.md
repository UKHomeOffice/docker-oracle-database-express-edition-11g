# Oracle Database Express Edition 11g Container

This provides a docker container for Oracle XE 11g.

## Usage

### Basic Usage

Due to licensing problems we cannot distribute the oracle RPM.

However this doesn't mean the setup process has to be horribly complicated. Simply create a new docker file that extends this docker file, place the [zip from oracle with the RPM in](http://www.oracle.com/technetwork/database/database-technologies/express-edition/downloads/index.html) a ```docker_files``` directory, and build it.

Your Dockerfile will be tiny and look like this

```Dockerfile
FROM ukhomeofficedigital/oracle-xe-11g:2.0.0
```

See /example if you're not sure what I mean.

### Volumes

Data is stored to the volume ```/u01/app/oracle```
 
### Customise the database on first run

The container will try to run ```/init_only.sh``` before running Oracle XE if there aren't any data files. You can use this script to initialise your database, simply add it in the container you have created which extends this one.

## Version Compatibility

This was built for oracle-xe-11.2.0-1.0, however with minor tweaks it would probably work for other versions.

# Docker tags

We use [SemVer](http://semver.io/) for the version tags available See the tags on this repository. 

# Find us

##  Docker repository
[ukhomeofficedigital/oracle-xe-11g](https://registry.hub.docker.com/u/ukhomeofficedigital/oracle-xe-11g)

## GitHub
[UKHomeOffice/docker-oracle-database-express-edition-11g](https://github.com/UKHomeOffice/docker-oracle-database-express-edition-11g)


# Contributing

Feel free to create pull requests or issues. 

Please note that this project is released with a [Contributor Code of Conduct](https://github.com/UKHomeOffice/docker-oracle-database-express-edition-11g/blob/master/code_of_conduct.md). By participating in this project you agree to abide by its terms.
