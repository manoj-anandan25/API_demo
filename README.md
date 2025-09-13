## Drink API – Flask + SQLite
durga devi ammma mariamma 
A simple RESTful API built using **Python**, **Flask**, and **SQLite** that allows you to manage a collection of drinks (e.g., Lemonade, Coffee).  
This project is great for learning how APIs work, testing backend skills, or building SDK demos.


---

 Features

-  View all drinks
-  View a drink by ID
-  Add a new drink
-  Delete a drink

---

Base URL

```

[http://localhost:5000](http://localhost:5000)

````


 Quick Start

 1. Install dependencies

```bash
pip install flask flask_sqlalchemy
````

 2. Run the app

```bash
python app.py
```

App will be running at:
👉 `http://localhost:5000`

---

 API Documentation

 `GET /drinks`

Returns a list of all drinks.

Response:

```json
{
  "drinks": [
    {
      "name": "Lemonade",
      "description": "Cool and refreshing"
    },
    {
      "name": "Espresso",
      "description": "Strong and bold"
    }
  ]
}
```

---

 `GET /drinks/<id>`

Returns a single drink by its ID.

Example:

```
GET /drinks/1
```

Response:

```json
{
  "name": "Lemonade",
  "description": "Cool and refreshing"
}
```

---

`POST /drinks`

Adds a new drink.

Request Header:

```
Content-Type: application/json
```

Request Body:

```json
{
  "name": "Green Tea",
  "description": "Healthy and light"
}
```

Response:

```json
{
  "id": 4
}
```

---

 `DELETE /drinks/<id>`

Deletes a drink by its ID.

Example:

```
DELETE /drinks/1
```

Response:

```json
{
  "message": "yeet!@"
}
```

---

 Testing Tools

You can test this API using:

* [Postman](https://www.postman.com/)


---

SDK / Frontend Integration Tips

* Set header: `Content-Type: application/json`
* Handle 404 and 500 errors properly
* Send JSON payloads as shown above
* Use `GET`, `POST`, `DELETE` methods only (for now)

---

Dev Notes

* Make sure `data.db` gets created in the project folder. 
* You can manually inspect the DB using `flask shell` or a SQLite viewer.
* Can be extended easily with `PUT` / `PATCH` for updates.

---





