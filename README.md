# ApexPlanet Task 3 — User Management System

PHP + MySQL project demonstrating CRUD, user authentication, role-based access, and profile management.

## Features
- Registration with server-side validation and `password_hash()`
- Login/logout with PHP sessions and `password_verify()`
- Admin-only user CRUD, search, pagination, and role editing
- User profile editing, bio/phone fields, and profile picture upload
- PDO prepared statements, CSRF tokens, escaped output, and input validation
- Responsive interface, password show/hide, password strength feedback
- Optional JSON email availability endpoint

## Run locally with XAMPP
1. Extract this folder into `C:\xampp\htdocs\ApexPlanet_Task3_User_Management_System`.
2. Start Apache and MySQL in XAMPP.
3. Open `http://localhost/phpmyadmin`, select Import, and import `database/schema.sql`.
4. Confirm DB settings in `config/config.php` (defaults: root user, blank password).
5. Visit `http://localhost/ApexPlanet_Task3_User_Management_System/setup-admin.php` and create the first admin.
6. **Immediately delete `setup-admin.php` after admin creation.**
7. Visit `http://localhost/ApexPlanet_Task3_User_Management_System/` and log in.
8. Register a test user; as admin, test add/edit/delete and search. As a user, test profile editing and upload.

## Upload rules
JPG, PNG, or WEBP only, maximum 2 MB. Uploaded filenames are random and image content is checked.

## Security
Public registration only creates `user` accounts. Admin role is assigned via one-time setup or by an existing admin. Forms use CSRF tokens; SQL uses PDO prepared statements; passwords are hashed. For production use HTTPS, least-privilege DB credentials, rate limiting, secure cookie settings, backups, and store uploads outside executable web paths. Never deploy with default local credentials.

## Files
- `database/schema.sql` — database/table setup
- `database/ER-DIAGRAM.md` — data model
- `DEMO-SCRIPT.md` — approximate 8-minute video outline
- `TASK-3-CHECKLIST.md` — testing/submission checklist
