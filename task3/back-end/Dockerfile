# Use the latest Ubuntu image as the base
FROM ubuntu:latest

# Update and upgrade packages
RUN apt-get update && apt-get upgrade -y

# Install Python 3 and pip
RUN apt-get install -y python3 python3-pip

RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask and flask cors with pip3
RUN pip3 install --no-cache-dir flask flask-cors

# Workdir and app code
WORKDIR /app
COPY ./api.py /app/api.py

# Expose the Flask port
EXPOSE 5252

# Default command: run the Flask app
CMD ["python3", "api.py"]
