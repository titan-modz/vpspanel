FROM ubuntu:22.04
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y python3 python3-pip nodejs npm docker.io curl git &&         pip3 install --no-cache-dir flask flask-cors flask-socketio docker python-dotenv sqlalchemy passlib bcrypt
WORKDIR /app
COPY . /app
EXPOSE 5000
# Run admin initialization then start the app
CMD ["bash", "-lc", "python3 backend/init_admin.py && python3 backend/app.py"]
