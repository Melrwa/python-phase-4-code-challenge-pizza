# Pizza-Restaurant API

A simple Flask RESTful API to manage restaurants, pizzas, and their relationships.

## Features

- **Restaurants**: Create, view, and delete restaurants.
- **Pizzas**: Add and view pizza details.
- **Restaurant-Pizza**: Link pizzas to restaurants with a validated price (1–30).
- **Error Handling**: Clear messages for invalid data or missing resources.

## Endpoints

### Restaurants

- `GET /restaurants` – List all restaurants.
- `GET /restaurants/<int:id>` – Get details of a restaurant.
- `DELETE /restaurants/<int:id>` – Delete a restaurant.

### Pizzas

- `GET /pizzas` – List all pizzas.
- `POST /pizzas` – Add a new pizza.

### Restaurant-Pizzas

- `POST /restaurant_pizzas` – Link a pizza to a restaurant with a price.

## Setup

1. **Clone Repository**

   ```bash
   git clone https://github.com/Melrwa/python-phase-4-code-challenge-pizza.git
   cd python-phase-4-code-challenge-pizza
   ```

## Install Dependencies

```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Setup Database

```bash
flask db init
flask db migrate
flask db upgrade
```

## Run Server

```bash
flask run
```

## Example Request

## POST /restaurant_pizzas

**Request:** 

```json

{
  "price": 15,
  "pizza_id": 1,
  "restaurant_id": 2
}
```

**Response:**

```json
{
  "id": 1,
  "price": 15,
  "pizza": { "id": 1, "name": "Margherita" },
  "restaurant": { "id": 2, "name": "Pizza Paradise" }
}
```

## License

This project is open-source and available under the MIT License. Feel free to modify and use it as needed!
