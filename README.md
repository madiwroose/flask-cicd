Flask CI/CD Kubernetes Demo 🚀
This project demonstrates a complete DevOps pipeline:
✅ A simple Flask web application
✅ Containerized with Docker
✅ Deployed to a Kubernetes cluster
✅ Fully automated using GitHub Actions CI/CD

🛠️ Tech Stack
- Flask - Python Web Framework
- Docker - Containerization
- GitHub Actions - CI/CD Automation
- Kubernetes - Container Orchestration
- DockerHub - Container Registry

📁 Project Structure
flask-cicd/
├── app.py                # Flask app code
├── Dockerfile            # Image build instructions
├── requirements.txt      # Python dependencies
├── .dockerignore         # Files ignored during Docker build
├── deployment.yaml       # Kubernetes deployment configuration
└── .github/
    └── workflows/
        └── ci.yml        # GitHub Actions workflow

🚀 How It Works
1. Flask Web App: A simple Flask API that returns a welcome message.
2. Docker Container: Packaged into a Docker image using python:3.9-slim.
3. Kubernetes Deployment: App is deployed in a Kubernetes cluster.
4. GitHub Actions CI/CD: Automates the full pipeline.

⚙️ Prerequisites
- DockerHub account
- Kubernetes cluster (minikube or cloud)
- Docker and kubectl installed
- GitHub repository with Secrets:
  - DOCKER_USERNAME
  - DOCKER_PASSWORD

✅ Setup & Run
1. Clone the Repo
   git clone https://github.com/YOUR_USERNAME/flask-cicd.git
   cd flask-cicd

2. Run Locally (Optional)
   pip install -r requirements.txt
   python app.py

3. Build Docker Image
   docker build -t your-dockerhub-username/flask-cicd .

4. Push to DockerHub
   docker login -u your-dockerhub-username
   docker push your-dockerhub-username/flask-cicd

5. Deploy to Kubernetes
   kubectl apply -f deployment.yaml

🔁 GitHub Actions Automation
When you git push, GitHub Actions:
- Builds and pushes the image
- (Optional) Can trigger your deployment pipeline

🧪 Testing
Visit the service (via Kubernetes service or port-forward):
kubectl port-forward deployment/flask-cicd-deployment 5000:5000
Then navigate to:
http://localhost:5000/

📄 License
MIT License

👨‍💻 Author
Hammad Ahmad
DevOps Engineer
GitHub: https://github.com/madiwroose

![image](https://github.com/user-attachments/assets/3091d1f5-a236-40b9-b29e-dbe445e74d59)
