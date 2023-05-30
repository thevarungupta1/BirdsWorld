# BirdsWorld
NodeJS application with MongoDB created for the Datadog course

## Development
1. To start developing locally, clone the project:

    ```sh
    git clone https://github.com/em4o/BirdsWorld.git
    ```
2.  Install the dependencies:

    ```sh
    npm install
    ```
3.  Run the application:

    ```sh
    npm run start
    ```
    
4.  Navivate to Swagger Link:

    ```sh
    http://localhost:3001/swagger/
    ```
    
5.  Install DD-Trace:

    ```sh
    npm install dd-trace --save
    ```
    
6. Add Configuration

    ```sh
    const tracer = require('dd-trace').init()
    const span = tracer.startSpan('web.request')

    span.setTag('dev', 'web')
    span.finish()
    ```