# Dockerfile Bug: Missing Dependency File

This repository demonstrates a common error in Dockerfiles: failure to include a necessary file (requirements.txt in this case).  The provided Dockerfile attempts to install Python packages using pip, but the requirements file is missing, leading to a build failure.

The `DockerfileFixed` provides a corrected version which includes the requirements.txt file, resolving the build issue.

## How to reproduce the bug

1. Clone this repository.
2. Attempt to build the image using the original `Dockerfile`:
   ```bash
docker build -t my-app .
```
3. Observe the build failure due to the missing `requirements.txt`.

## How to fix the bug

1. Use the corrected `DockerfileFixed` to build the image:
   ```bash
docker build -t my-app -f DockerfileFixed .
```
2. Verify that the image builds successfully.