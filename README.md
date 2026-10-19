# Social Network API

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python manage.py makemigrations accounts profiles chats groups_app channels_app posts
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Swagger: http://127.0.0.1:8000/swagger/
ReDoc: http://127.0.0.1:8000/redoc/

## Authentication

Register at `POST /api/accounts/register/` with `phone_number` and `password`.
Get JWT at `POST /api/accounts/token/` with the same fields.
Use `Authorization: Bearer <access_token>`.

## Main endpoints

- `POST /api/accounts/register/`
- `POST /api/accounts/token/`
- `POST /api/accounts/token/refresh/`
- `GET /api/accounts/me/`
- `POST /api/accounts/change-password/`
- `POST /api/accounts/logout/`
- `GET /api/profiles/`
- `GET/PATCH /api/profiles/me/`
- `GET /api/profiles/{id}/`
- `POST /api/avatars/`
- `GET/DELETE /api/avatars/{id}/`
- `GET/POST /api/chats/`
- `GET/DELETE /api/chats/{id}/`
- `GET/POST /api/chats/{chat_id}/messages/`
- `DELETE /api/messages/{id}/`
- `GET/POST /api/groups/`
- `GET/PATCH/DELETE /api/groups/{id}/`
- `GET/POST /api/groups/{group_id}/members/`
- `PATCH /api/groups/{group_id}/members/{id}/`
- `DELETE /api/groups/{group_id}/members/me/`
- `GET/POST /api/groups/{group_id}/messages/`
- `DELETE /api/group-messages/{id}/`
- `GET/POST /api/channels/`
- `GET/PATCH/DELETE /api/channels/{id}/`
- `POST/DELETE /api/channels/{channel_id}/follow/`
- `GET /api/following/`
- `GET /api/channels/{channel_id}/is-following/`
- `GET/POST /api/channels/{channel_id}/posts/`
- `GET/PATCH/DELETE /api/posts/{id}/`
# telegram
