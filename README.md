🌱 Soil Management System

A simple web-based Soil Management System using Streamlit and MySQL to manage soil health records. The system allows users to manually insert soil test data, generate bulk random records, and view stored records in a table.

📂 Project Structure

📦 Soil Management System  
├── soil_management.py       # Main Streamlit application  
└── README.md                # Project documentation  

📊 Database Schema (soil_health)

CREATE TABLE IF NOT EXISTS soil_health (
    record_no INT AUTO_INCREMENT PRIMARY KEY,
    farm_location VARCHAR(255) NOT NULL,
    test_date DATE,
    nitrogen_level FLOAT,
    phosphorus_level FLOAT,
    potassium_level FLOAT,
    pH_level FLOAT,
    moisture_content FLOAT
);

⚙️ Setup Instructions
	1.	Install Dependencies

pip install streamlit mysql-connector-python faker pandas

	2.	Configure Database
Update the database credentials in soil_management.py:

DB_CONFIG = {
    "host": "localhost",
    "user": "root",
    "password": "YOUR_MYSQL_PASSWORD",
    "database": "soil_management"
}

	3.	Create the Database
Log into MySQL and run:

CREATE DATABASE soil_management;

	4.	Run the Application
Start the Streamlit app:

streamlit run soil_management.py

	5.	Access the App
Open your browser and go to:

http://localhost:8501

🚀 How to Use
	•	Insert Manual Record: Fill in the form and click Insert Record.
	•	Insert Bulk Records: Select a quantity and click Insert Bulk Records.
	•	View Records: Choose a limit or view all records in the table.

