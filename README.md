# 🧾 Expense Tracker

This **Expense Tracker** helps you manage daily expenses with ease. Built with **FastAPI** (Backend), **Streamlit** (Frontend), and **MySQL** as the database.
![Expense Tracker UI](https://user-images.githubusercontent.com/12345678/UI1.png)
![Expense Tracker UI](frontend/UI3.png)
![Expense Tracker UI](frontend/UI4.png)

---

## 🗂 Project Structure

expense_tracker/ │ ├── backend/ │ ├── main.py # FastAPI app │ ├── models.py # Pydantic models │ ├── crud.py # Database operations │ └── database.py # MySQL connection │ ├── frontend/ │ └── app.py # Streamlit user interface │ ├── requirements.txt # Project dependencies └── README.md # Project documentation

---

## ⚙️ Setup Instructions

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/expense_tracker.git
   cd expense_tracker
   ```
2. **Install dependencies:**:   
   ```commandline
    pip install -r requirements.txt
   ```
3. **Run the FastAPI server:**:   
   ```
    # From project root, if using terminal:
    uvicorn backend.main:app --reload

    # Or, from PyCharm terminal:
    uvicorn main:app --reload

   ```
4. **Run the Streamlit app:**:   
   ```commandline
    streamlit run frontend/app.py
   ```
5. **Configure MySQL Database**:   
   ```Ensure MySQL is running and create a database:
      CREATE DATABASE expense_tracker;

      USE expense_tracker;

      CREATE TABLE expenses (
          id INT AUTO_INCREMENT PRIMARY KEY,
          date DATE NOT NULL,
          category VARCHAR(100) NOT NULL,
          amount DECIMAL(10,2) NOT NULL,
          payment_method VARCHAR(50) NOT NULL,
          description TEXT
      );
      Update your backend/database.py file with the correct MySQL credentials.
   ```
6. **API Endpoints:**
   ```
   Method	Endpoint	Description
   GET	       /expenses	Get all expenses
   POST	       /expenses	Add a new expense
   PUT	       /expenses/{id}	Update an expense by ID
   DELETE      /expenses/{id}	Delete an expense by ID
   ```
   
