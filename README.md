# Setup Instructions - Dušan Jolović

# Additional Thoughts

Security: Implement proper authentication and authorization mechanisms to protect sensitive employee data.

Validation: Enhance input validation to ensure data integrity and security. Validate CSV file format and content more thoroughly.

Performance: Optimize database queries for better performance, especially when dealing with large datasets.

Error Handling: Implement comprehensive error handling and logging to troubleshoot issues effectively.

Testing: Develop unit tests and integration tests to verify the functionality and reliability of the API.

# INSTRUCTIONS

1. Download/clone this repository to your local machine.

2. Configure your database settings in the `.env` file:

   ```makefile
   DB_CONNECTION=mysql
   DB_HOST=your_database_host
   DB_PORT=your_database_port
   DB_DATABASE=your_database_name
   DB_USERNAME=your_database_username
   DB_PASSWORD=your_database_password

3. Install dependencies using Composer:
    ```makefile
    composer install

4. Run database migrations to create the necessary tables and start the server:
    ```makefile
    php artisan migrate
    php artisan serve

# Employee Management
```makefile
GET /api/employee
Retrieve a list of all employees.

GET /api/employee/{id}
Retrieve a specific employee by their ID.

DELETE /api/employee/{id}
Delete a specific employee by their ID.

BATCH UPLOAD: 

curl -X POST -F "import=@import.csv" http://127.0.0.1:8000/api/employee/
