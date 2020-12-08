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
            │   │   ├── models.py
            │   │   └── ping.py
            │   ├── db.py
            │   └── main.py
            ├── requirements.txt
            └── tests
                ├── __init__.py
                ├── conftest.py
                └── test_main.py

* Docker


    $ docker-compose up -d --build
    $ docker-compose exec web pytest .



*************************
    http://http://0.0.0.0:8002/ping
    {
      "ping": "pong!"
    }

    http://http://0.0.0.0:8002/docs    
    http://0.0.0.0:8002/redoc

***********************
    Routes

    set up the basic CRUD routes, following RESTful best practices:
    
    Endpoint 	    HTTP Method 	CRUD Method 	Result
    /notes/ 	    GET 	        READ 	        get all notes
    /notes/:id/ 	GET 	        READ 	        get a single note
    /notes/ 	    POST 	        CREATE 	        add a note
    /notes/:id/ 	PUT 	        UPDATE 	        update a note
    /notes/:id/ 	DELETE 	        DELETE 	        delete a note
***************************
Postgres 
 
    DATABASE_URL=postgresql://postgres:postgres@db/fastapi_dev
    - POSTGRES_USER=postgres
    - POSTGRES_PASSWORD=postgres
    - POSTGRES_DB=fastapi_dev


databases is an async SQL query builder that works on top of the SQLAlchemy Core expression language. It supports the following methods:

    database.fetch_all(query)
    database.fetch_one(query)
    database.iterate(query)
    database.execute(query)
    database.execute_many(query)

Review the Async SQL (Relational) Databases guide and the Starlette Database docs for more details on working with databases asynchronously.

***************************
Models

    check db:
    $ docker-compose exec db psql --username=postgres --dbname=fastapi_dev
    # \l
    # \dt
    # \q

Pydantic Model (like serializer in drf)
https://pydantic-docs.helpmanual.io/
*******************************************
