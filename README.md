# Report API
The API is to report the cloud instances

# Verify using the deployed docker image(Docker Hub):
Make sure the docker is installed in the machine.
Run docker run -p 9000:9000 farheenaslam/report-service:latest
The server runs on port 9000. The API can be accessed at http://localhost:9000

# Set up to run locally:
Make sure Python is installed and set in path variable
Run pip install -r requirement.txt . This is to be first time to make sure all the dependencies are resolved
Run python run_backend.py
The server is listening to port 9000. The API can be accessed at http://localhost:9000

# Steps to deploy the docker:
Make sure Python is installed and set in path variable
docker build -t farheenaslam/report-service:latest .
docker image ls
docker run -d -p 9000:9000 farheenaslam/report-service:latest .

# Steps to deploy the docker(Docker Hub):
Make sure the docker is installed in the machine.
docker build -t farheenaslam/report-service:latest .
docker push farheenaslam/report-service:latest
Run docker run -p 9000:9000 farheenaslam/report-service:latest
The server runs on port 9000. The API can be accessed at http://localhost:9000

# Steps to execute the pytest
Make sure pyTest is installed and other dependencies mentioned in requirement.txt
From the project root folder, run python -m pytest --html=report.html tests/
Executes all the test and the result is in html format in the project root named report.html

![image](https://user-images.githubusercontent.com/16043374/172958784-242ad13c-7b98-44d9-bfb1-9427a188fae2.png)





