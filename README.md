FastAPI 

* Dependencies:


    FastAPI v0.46.0
    Docker v19.03.5
    Python v3.8.1
    Pytest v5.3.2
    Databases v0.2.6
    


* Project structure


    fastapi-crud
        ├── docker-compose.yml
        ├── .gitignore
        ├── README.md
        └── src
            ├── Dockerfile
            ├── app
            │   ├── __init__.py
            │   ├── api
            │   │   ├── __init__.py
            │   │   └── ping.py
            │   └── main.py
            ├── requirements.txt
            └── tests
                ├── __init__.py
                ├── conftest.py
                └── test_ping.py