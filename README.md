# Oracle Database Express Edition 11g Container

This provides a docker container for Oracle XE 11g.

## Usage

Due to licensing problems we cannot distribute the oracle RPM.

However this doesn't mean the setup process has to be horribly complicated. Simply create a new docker file that extends this docker file, place the [zip from oracle with the RPM in](http://www.oracle.com/technetwork/database/database-technologies/express-edition/downloads/index.html) in the same directory, and build it.

Your Dockerfile will be tiny and look like this

```Dockerfile
FROM purplebooth/oracle-xe-11g:0.1.0
```

See /example if you're not sure what I mean.

## Version Comparability

This was built for oracle-xe-11.2.0-1.0, however with minor tweaks it would probably work for other versions. This is untested.

### Docker tags

We use [SemVer](http://semver.io/) for the version tags available See the tags on this repository. 
