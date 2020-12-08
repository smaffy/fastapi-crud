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