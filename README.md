# Customer360 Django Application

This is a Django web application designed to manage customer interactions, allowing users to record and track communication with their customers.

## Features

*   **Customer Management:**
    *   Add new customers with details like name, email, phone, address, and social media (optional).
    *   View a list of customers on the landing page with their details.
    *   Select a customer to record interactions.
*   **Interaction Tracking:**
    *   Record interactions with customers, specifying the channel, direction (inbound/outbound), and a summary of the communication.
    *   Uses multiple interaction channels, including `phone`, `sms`, `email`, `letter`, and `social media`.
    *  Interaction summaries can be added as free-form text
*   **Interaction Summary:**
    *   View a summary of interactions within the last 30 days, grouped by channel and direction.
    *   Displays the count of interactions for each channel and direction combination.
    * Shows a total count of interactions in the last 30 days.
*   **User Interface:**
    *   User-friendly interface with Bootstrap for styling and responsive design.
    *   Uses clean and consistent layout.
* **Basic Form Validation**:
    *  The form for adding interactions uses javascript to make sure the user selects a direction, channel and writes a summary before submitting the form.
*  **Clear View Logic**:
    *  Views manage the logic for saving and showing data.

## Setup Instructions

Follow these steps to set up and run the application:

1.  **Clone the Repository** (Assuming you have a git repository)

    ```bash
    git clone https://github.com/JayJay247in/djangoApp_Customer360.git
    cd djangoApp_Customer360
    ```

2.  **Create a Virtual Environment** (Recommended)
    ```bash
    pip install virtualenv
    virtualenv djangoenv
    source djangoenv/bin/activate  # On Linux/macOS
    djangoenv\Scripts\activate # On windows
    ```
    ```
     # If using powershell
    .\djangoenv\Scripts\activate
    ```

3.  **Install Dependencies:**

    ```bash
    python -m pip install -r requirements.txt
    ```
   (Make sure a requirements.txt file is present with the required django and other packages used. If not, create this with the command `pip freeze > requirements.txt`)

4.  **Apply Migrations:**

    ```bash
    python manage.py makemigrations interactions
    python manage.py migrate
    ```

5.  **Run the Development Server:**

    ```bash
    python manage.py runserver
    ```

6.  **Access the Application:**
    *   Open your web browser and go to `http://127.0.0.1:8000/`

## Project Structure

The project follows a standard Django application structure:

*   `customer360/` (Project root directory):
    *   `customer360/` (Project settings and URLs)
        *   `settings.py`: Configuration file for the project.
        *   `urls.py`:  Main URL configuration.
    *   `interactions/`: (Django app containing the core logic)
        *  `models.py`: Defines the `Customer` and `Interaction` database models.
        *  `forms.py`: Defines the forms for adding interactions.
        *   `views.py`: Contains the view functions for handling requests.
        *   `urls.py`: URL configuration for the `interactions` app.
        *   `templates/interactions/`: HTML templates for rendering web pages.
        *   `static/css/`: Location for static CSS files, like `main.css`
    *  `manage.py`: Django utility for running commands.
    * `db.sqlite3`: The database for saving data.

## Optional Modifications

The application can be further enhanced with the following modifications:

*   **Add a social_media field to the Customer model**: This allows the user to track the social media profile for the customers.
*   **Add `social_media` as a new interaction channel**: This allows users to register interactions with customers that happen on social media.
*   **Improved User Authentication:** Add user accounts to track who created which record.
*   **Search and Filtering:** Allow filtering by channel, direction, and date ranges.
*   **Edit and Delete:** Enable editing and deleting of existing interactions and customers.
*   **Pagination:** For a large number of interactions, consider pagination to display them in smaller chunks.
*   **Detail View:** Provide a detail view to show more information about each interaction.
*   **Add unit tests**: Add unit tests for testing specific functions or views.

## Technologies Used

*   Django (Web framework)
*   Python (Programming Language)
*   HTML, CSS, JavaScript (Frontend)
*  Bootstrap (CSS Framework)
*  Sqlite (Database)
## Author

IKECHUKWU FAITHFUL
cj193532@gmail.com