# Reference: https://towardsdatascience.com/docker-made-easy-for-data-scientists-b32efbc23165

# Pull the base ubuntu image
FROM ubuntu:latest

# Update apt to get the latest packages info (-y - no user input required)
RUN apt update -y 

# Install python
RUN apt install -y python3-pip

# Copy all contents of the directory into a folder in the image called app
COPY . /app

# Set app as the working directory (this is not really required)
WORKDIR /app

# Install required packages (in this case only flask)
# RUN pip3 install flask
RUN pip3 install -r requirements.txt

# Exposing port 5000 for the API (default Flask port)
EXPOSE 5000

# Setting the entrypoint
ENTRYPOINT ["python3"]

# Running our app.py api script inside our contrainer
CMD ["app.py"]
