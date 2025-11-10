# CI-with-GitHub

## Run the application with Docker

1. Build the Docker image:

    ```bash
    docker build -t flask-app:latest .
    ```

2. Start the container:

    ```bash
    docker run -p 5001:5001 flask-app:latest
    ```

    port 5001 is used here because port 5000 was already occupied.

---

## Implementation

### Docker setup

1. Obtain the project archive from Teams and extract it.

2. Create an isolated Conda environment to prevent dependency conflicts:

    ```bash
    conda create -n docker_exercise python=3.10
    ```

3. Install the required Python packages:

    ```bash
    pip install flask gunicorn
    ```

4. Export installed packages to requirements.txt:

    ```bash
    pip freeze > requirements.txt
    ```

5. Add a Dockerfile to the project and populate it with the build instructions for the Flask application.

6. Create a .dockerignore file and list files or directories that should be excluded from the build context (for example, virtual environments, local data, and large artifacts).

7. Build the Docker image:

    ```bash
    docker build -t flask-app:latest .
    ```

8. Run the container:

    ```bash
    docker run -p 5001:5001 flask-app:latest
    ```

    port 5001 is used here because port 5000 was already occupied.

---

### GitHub setup

1. Initialize the local Git repository and commit the project:

    ```bash
    git init
    git add .
    git commit -m "Initial project + Dockerfile"
    ```

2. Create a new repository on GitHub via the website or CLI.

3. Link the local repo to the remote origin:

    ```bash
    git remote add origin https://github.com/akksel1/docker_exercise.git
    ```

4. Push the local commits to the remote:

    ```bash
    git push -u origin master
    ```