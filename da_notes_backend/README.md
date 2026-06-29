# DA Notes Backend

This is a Django REST Framework backend for the DA Notes Angular app.

## API

- `GET /notes/` - list notes
- `POST /notes/` - create a note
- `GET /notes/<id>/` - retrieve a note
- `PUT /notes/<id>/` - update a note
- `PATCH /notes/<id>/` - partial update a note
- `DELETE /notes/<id>/` - delete a note

## Setup

### Windows

1. Open PowerShell in the backend folder.
2. Create and activate a virtual environment:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Run migrations:

```bash
python manage.py makemigrations
python manage.py migrate
```

5. Start the server:

```bash
python manage.py runserver 127.0.0.1:8000
```

## Frontend connection

The Angular frontend uses a dev proxy and sends requests to:

- `http://localhost:4200/notes/`

The proxy forwards that path to:

- `http://127.0.0.1:8000/notes/`
