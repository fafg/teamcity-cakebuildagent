# teamcity-cakebuildagent
this repo has the docker file to build a teamcity agent with dotnet core 2.2 and mono to be used with cake scripts

## build
    ```shell
    docker build -f DOCKERFILE -t <user/reponame:tag> . 
    ```
## usage
    ```shell
    docker run -dit -e SERVER_URL="https://teamcity.jetbrains.com/" -v <path to agent config folder>:/data/teamcity_agent/conf --name cakebuild fafg/teamcity-cake-agent-aspnetcore
    ```

    Take a look at buildagent.properties for more options. Mount the volume to this file path.

## Example 
    Please access this [repo](https://github.com/fafg/teamcity-cake-ci-cd-docker-swarm) to see a cake build example

## docker image
    [teamcity agent to use with cake and aspnet core 2.2](https://hub.docker.com/r/fafg/teamcity-cake-agent-aspnetcore/)