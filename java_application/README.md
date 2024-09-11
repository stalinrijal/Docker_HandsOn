Build the Docker Image:
To build the Docker image, run the following command:

docker build -t java-hello-world .

Run the Docker Container:
To run the container, use the command below:

docker run -p 8080:8080 java-hello-world

Access the Application:
Now you can access the application by navigating to http://localhost:8080 in your browser, and you should see the message:

Hello, World!