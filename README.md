# ☁️ Cloud DevOps Project

This project demonstrates a complete DevOps lifecycle implementation for deploying a Flask web application on the cloud using the following tools:

- **Git & GitHub** – Source control and collaboration
- **Docker** – Containerization
- **Kubernetes (K8s)** – Container orchestration
- **Terraform** – Infrastructure as Code on AWS
- **Ansible** – Configuration management
- **Jenkins** – Continuous Integration (CI)
- **ArgoCD** – Continuous Deployment (CD)

---

## 📦 Application Overview

The application is a simple Python Flask web app that renders an HTML page using Jinja templates.

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route("/")
def index():
    return render_template("index.html")

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)
```

## 1- Docker 

Dockerfile builds the Flask app into a container image.

```
docker build -t flask-app .

docker run -p 5000:5000 flask-app
```

<img width="986" height="646" alt="image" src="https://github.com/user-attachments/assets/f0d77ea1-a8b8-4ce7-8ccd-fcafffb22b41" />
