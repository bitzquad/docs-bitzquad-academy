# Contributing

## Prerequisites
- Python^3.6
- Git
- Code Editor

## Using Docker (Recommended)
1. Start Development Server
```
git clone https://github.com/bitzquad/docs-bitzquad-academy.git
cd docs-bitzquad-academy
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```
2. Build Documentation
```
docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build
```

## Installation
1. Install Python.
    - Windows: https://www.python.org/downloads/windows/
    - Linux/Ubuntu: 

        ```
        sudo apt update
        sudo apt install software-properties-common
        sudo add-apt-repository ppa:deadsnakes/ppa
        sudo apt update
        sudo apt install python
        ```
2. Install `mkdocs` on your local machine.
    
    ```
    pip install mkdocs
    ```
    or
    ```
    pip3 install mkdocs
    ```

3. Clone the repository.
    ```
    git clone https://github.com/bitzquad/docs-bitzquad-academy.git
    cd docs-bitzquad-academy
    ```

4. Install all the dependancies.

    ```
    pip install -r requirements.txt
    ```
    or
    ```
    pip3 install -r requirements.txt
    ```
## Deploy Locally

1. On Windows:
    ```
    python -m mkdocs serve
    ```
2. On Linux/Ubuntu
    ```
    mkdocs serve
    ```
Open up `http://127.0.0.1:8000/` in your browser, and you'll see the home page of the documentation.

## Build Locally

1. On Windows:
    ```
    python -m mkdocs build
    ```
2. On Linux/Ubuntu
    ```
    mkdocs build
    ```