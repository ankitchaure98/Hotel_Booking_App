# HotelApplication — Java + React

Aurelia Stays is a redesigned React frontend for the Spring Boot hotel backend.

## Run locally

### 1. Start MySQL
Use your existing MySQL setup, then confirm the database `hotel_app` exists and the credentials in
`src/main/resources/application.properties` match your database.

### 2. Start the Java backend
From the project root:

```bash
./mvnw spring-boot:run
```

Windows:
```bat
mvnw.cmd spring-boot:run
```

The API runs at `http://localhost:8080`.

### 3. Start the frontend
Open a second terminal:

```bash
cd frontend
npm install
npm start
```

Open `http://localhost:3000`.


<img width="1872" height="861" alt="image" src="https://github.com/user-attachments/assets/26c6f50b-d311-4c29-a467-6d3cf70559ab" />





The frontend uses `REACT_APP_API_URL` when provided; otherwise it defaults to
`http://localhost:8080/api`. A `.env.example` file is included.


## Run from Docker




## Available backend endpoints

- `POST /api/auth/register` ---> To Register for HOTELOWNER and CUSTOMER
- `GET /api/hotels` ---> To see the List of Hotels
- `POST /api/hotels`
- `GET /api/users` ---> To see the List of USERS
- `GET /test` ---> Test the application
The frontend includes login/register, JWT persistence, hotel listing, and hotel creation for
`ADMIN` or `HOTEL_OWNER` roles. The frontend is intentionally kept separate from the Java
backend so both can be developed independently.
