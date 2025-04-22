# 📝 Line-by-Line Explanation
## Dockerfile
```
FROM ubuntu:latest

WORKDIR /app

COPY . /app

RUN apt-get update && apt-get install -y python3 python3-pip

ENV NAME World

CMD ["python3", "app.py"]
```

---
```
FROM ubuntu:latest
```
Sets the base image to the latest version of Ubuntu.

All subsequent instructions in the Dockerfile will build on top of this base image.

---
```
WORKDIR /app
```
Sets the working directory inside the container to /app.

Any command (COPY, RUN, etc.) that follows will be executed from this directory.

If /app does not exist, it will be created automatically.

---
```
COPY . /app
```
Copies the contents of your current local directory (where the Dockerfile is located) into the /app directory inside the container.

For example, your app.py file will be available at /app/app.py.

---
```
RUN apt-get update && apt-get install -y python3 python3-pip
```
Updates the package list with apt-get update.

Installs Python 3 and pip using apt-get install.

The -y flag automatically confirms installation prompts.

---
```
ENV NAME World
```
Sets an environment variable named NAME with the value World.

In your Python app, this can be accessed using:

```
import os
name = os.getenv("NAME", "default")
```

---
```
CMD ["python3", "app.py"]
```
Defines the default command to run when the container starts.

This launches your Python app using the app.py file as the entry point.
