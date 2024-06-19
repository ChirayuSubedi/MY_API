
# Day 66 Cafe API

## Project Overview

This project is a Cafe API built using Python and Flask. It allows users to interact with a database of cafes, including retrieving information about cafes, adding new cafes, updating existing cafes, and deleting cafes.

## Contents

- `.DS_Store`: System file (not relevant to the project)
- `requirements.txt`: List of dependencies required to run the project
- `instance/`: Directory containing instance-specific files and configurations
- `templates/`: Directory containing HTML templates for rendering web pages
- `main.py`: The main Python file for the Flask application

## Setup and Installation

To set up and run the Cafe API project on your local machine, follow these steps:

### Prerequisites

- Python 3.x
- Flask

### Installation

1. **Clone the repository:**

   ```bash
   git clone <repository_url>
   cd day-66-cafe-api-end
   ```

2. **Create a virtual environment:**

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

### Running the Application

1. **Set up environment variables:**

   Create a `.env` file in the root directory and add necessary environment variables, such as:

   ```plaintext
   FLASK_APP=main.py
   FLASK_ENV=development
   SECRET_KEY=<your_secret_key>
   ```

2. **Initialize the database:**

   Ensure the database is set up correctly. This project assumes the use of SQLite for development.

   ```bash
   flask db init
   flask db migrate -m "Initial migration."
   flask db upgrade
   ```

3. **Run the Flask application:**

   ```bash
   flask run
   ```

   The application should now be running at `http://127.0.0.1:5000/`.

## Project Structure

- `instance/`: Contains configuration files and instance-specific data.
- `templates/`: Holds HTML templates for rendering web pages.
- `main.py`: The main application file where the Flask app is created and routes are defined.

## Usage

You can interact with the API using tools like Postman or cURL. The endpoints available include:

- `GET /cafes`: Retrieve a list of all cafes.
- `POST /cafes`: Add a new cafe.
- `PUT /cafes/<id>`: Update an existing cafe.
- `DELETE /cafes/<id>`: Delete a cafe by ID.

Refer to the code in `main.py` for more detailed information on the endpoints and their expected inputs/outputs.

## Contributing

If you wish to contribute to this project, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contact

For any questions or feedback, please reach out to the project maintainer.
