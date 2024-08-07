# Drink API

## Description

The Drink API is a simple RESTful API built with Django and Django REST Framework. It allows users to manage a list of drinks through basic CRUD operations. 

The key functionalities include: 
- Retrieving a list of all drinks
- Adding a new drink
- Retrieving the details of a specific drink by ID
- Updating the details of a specific drink by ID
- Deleting a specific drink by ID

## Installation Instructions

### Prerequisites

- Python 3.x
- Django
- Django REST Framework

### Steps

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your_username/drink_api.git
    ```
   
2. **Navigate to the project directory**:
    ```bash
    cd drink_api
    ```

3. **Create a virtual environment**:
    ```bash
    python -m venv venv
    ```

4. **Activate the virtual environment**:
    - On Windows:
      ```bash
      venv\Scripts\activate
      ```
    - On macOS and Linux:
      ```bash
      source venv/bin/activate
      ```

5. **Install the required dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

6. **Apply migrations**:
    ```bash
    python manage.py migrate
    ```

7. **Run the server**:
    ```bash
    python manage.py runserver
    ```

## Usage

After starting the Django server, the API endpoints can be accessed using an API client like Postman or via simple HTTP requests. The following endpoints are available:

### Endpoints

1. **Get All Drinks / Add a New Drink**:
    - **URL**: `/api/drinks/`
    - **Method**: GET, POST

2. **Get / Update / Delete a Specific Drink by ID**:
    - **URL**: `/api/drinks/{id}/`
    - **Method**: GET, PUT, DELETE

## Examples

### Retrieve All Drinks

**Request**:
```bash
GET /api/drinks/
```

**Response**:
```json
[
    {
        "id": 1,
        "name": "Coca Cola",
        "description": "A refreshing soft drink."
    },
    {
        "id": 2,
        "name": "Pepsi",
        "description": "Another popular soft drink."
    }
]
```

### Add a New Drink

**Request**:
```bash
POST /api/drinks/
```

**Request Body**:
```json
{
    "name": "Mountain Dew",
    "description": "A citrus-flavored carbonated beverage."
}
```

**Response**:
```json
{
    "id": 3,
    "name": "Mountain Dew",
    "description": "A citrus-flavored carbonated beverage."
}
```

### Retrieve a Specific Drink by ID

**Request**:
```bash
GET /api/drinks/1/
```

**Response**:
```json
{
    "id": 1,
    "name": "Coca Cola",
    "description": "A refreshing soft drink."
}
```

### Update a Specific Drink by ID

**Request**:
```bash
PUT /api/drinks/1/
```

**Request Body**:
```json
{
    "name": "Coca Cola Zero",
    "description": "A low-calorie soft drink."
}
```

**Response**:
```json
{
    "id": 1,
    "name": "Coca Cola Zero",
    "description": "A low-calorie soft drink."
}
```

### Delete a Specific Drink by ID

**Request**:
```bash
DELETE /api/drinks/1/
```

**Response**:
```bash
HTTP 204 No Content
```

