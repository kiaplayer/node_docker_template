# Template for nodejs environment in Docker

1. Install "Docker" and "Docker Compose".
2. Create new project folder if necessary (and place your application code here).
3. Copy files from this repo to your project folder.
4. Start container:
    ``` bash
    $ docker-compose build
    $ docker-compose run --rm --service-ports node
    ```
4. Install node modules:
    ``` bash
    (inside container) $ yarn install / npm install
    ```
5. Start your application (you need to bind your application server to "0.0.0.0:3000"):
    ``` bash
    (inside container) $ yarn dev / npm dev
    ```
6. Access your app in browser - http://localhost:3000