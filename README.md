# Fitness Booking App

## Setup
1. Clone the repository or download the zip file.
2. Delete fitness.db file if present
3. Install dependencies: `pip install -r requirements.txt`.
4. Run seed data: `python seed_data.py`.
5. Start the server: `uvicorn app.main:app --reload`.
6. Run tests: `pytest`.

## API Endpoints
- **GET /classes**: List upcoming classes.
  - cURL: `curl http://127.0.0.1:8000/classes?timezone=Asia/Kolkata`
- **POST /book**: Book a class.
  - cURL: `curl -X POST http://127.0.0.1:8000/book -d '{"class_id": 1, "client_name": "John", "client_email": "john@example.com"}' -H "Content-Type: application/json"`
- **GET /bookings**: Get bookings by email.
  - cURL: `curl http://127.0.0.1:8000/bookings?email=john@example.com`

## Notes
- Uses SQLite in-memory database.
- Timezone management with pytz.
- Error handling and logging included.
