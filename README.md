# SynBioHub Docker Setups
## Updated March 20, 2020

The docker-compose files in this repository represent various configurations for deploying SynBioHub.
The files can be layered with Docker Compose's [multiple file](https://docs.docker.com/compose/reference/overview/#specifying-multiple-compose-file) capabilities. 

The base configuration, described with `docker-compose.yml`, is simply SynBioHub, its graph database Virtuoso, and an autohealer.

To run the base configuration, simply use `docker-compose up`.

To add [SBOLExplorer](https://github.com/michael13162/SBOLExplorer), add the `docker-compose.explorer.yml` to the main docker-compose.

To run the configuration with SBOLExplorer, use `docker-compose -f docker-compose.yml -f docker-compose.explorer.yml up`.

To add iGEM rendering plugins, add the `docker-compose.igem.yml`.

To run the configuration with iGEM, use `docker-compose -f docker-compose.yml -f docker-compose.igem.yml up`.

The `docker-compose.version.yml` can be added to another configuration, and simply contains the latest version of the SynBioHub docker image. 
This version does not even contain the Virtuoso image, so it should only be used by someone who knows what they are doing. 