# Building a Single-Page-App with Micronaut and VueJS  #

This is a copy of the [micronaut-spa-react](https://github.com/micronaut-guides/micronaut-spa-react) repository, modified to include a VueJS - based single page application, instead of React.

The original React - based guide is available at http://guides.micronaut.io/micronaut-spa-react/guide/index.html

This repository also contains a modified version of the Guide, with instructions changed for the VueJS client.

The `/initial` folder can be used to walk through the guide.  The `/complete` folder is another version, with all of the guide steps completed.

## Running (summary)

To build and run the client SPA:

```shell
cd complete/client
yarn serve
```

To build and run the Micronaut server:

```shell
cd complete/server
./gradlew run
```

To build and run an executable jar containing both client and server code:

```shell
cd complete
./gradlew assembleServerAndClient
java -jar server/build/libs/server-0.1-all.jar
```




