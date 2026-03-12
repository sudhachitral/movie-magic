🎬 Movie Magic – Movie Ticket Booking System

Movie Magic is a web-based movie ticket booking application built using Flask and AWS services.
The system allows users to browse movies, book tickets, manage profiles, and receive booking confirmations.
An admin panel is also provided to manage movies.

🚀 Features
👤 User Features

User Signup and Login with secure password hashing

Browse available movies

View movie details

Book movie tickets

Simulated payment system

Booking confirmation

Email notification using AWS SNS

User profile management

Booking history

🛠️ Admin Features

Admin login

Add new movies

Edit movie details

Delete movies

Manage movie listings

🧰 Technologies Used
Backend

Python

Flask

Frontend

HTML

CSS

Bootstrap

Cloud Services (AWS)

AWS EC2 – Application hosting

AWS DynamoDB – Database for users, movies, and bookings

AWS SNS – Email notifications

Libraries

boto3

werkzeug

uuid

datetime

🗄️ Database Tables (DynamoDB)
1️⃣ MovieMagic_Users

Stores user information.

Fields:

email (Primary Key)

id

name

password

theme

first_name

last_name

mobile

birthday

gender

married

2️⃣ MovieMagic_Movies

Stores movie details.

Fields:

movie_id (Primary Key)

title

genre

language

duration

rating

price

theater

address

description

image

trailer

3️⃣ MovieMagic_Bookings

Stores booking information.

Fields:

booking_id (Primary Key)

movie_name

theater

date

time

seats

amount_paid

address

booked_by

user_name

payment_id

booking_time

📂 Project Structure
movie-magic
│
├── app.py
├── templates
│   ├── index.html
│   ├── login.html
│   ├── signup.html
│   ├── dashboard.html
│   ├── movie_details.html
│   ├── booking.html
│   ├── payment.html
│   ├── confirmation.html
│   ├── profile.html
│   └── admin.html
│
├── static
│   ├── css
│   ├── js
│   └── images
│
└── README.md
⚙️ Installation & Setup
1️⃣ Clone the repository
git clone https://github.com/sudhachitral/movie-magic.git
2️⃣ Navigate to project folder
cd movie-magic
3️⃣ Install dependencies
pip3 install flask boto3 werkzeug
☁️ AWS Configuration

Create the following DynamoDB tables:

MovieMagic_Users

MovieMagic_Movies

MovieMagic_Bookings

Create an SNS Topic for email notifications.

Example:

MovieTicketNotifications
▶️ Running the Application

Start the Flask server:

python3 app.py

Application runs at:

http://localhost:5000

For EC2 deployment:

http://YOUR_PUBLIC_IP:5000
🔐 Admin Login

Admin credentials:

Email: admin@moviemagic.com
Password: admin123
📧 Email Notifications

When a booking is confirmed, the system sends a ticket confirmation email using AWS SNS.

📌 Future Improvements

Online payment gateway integration

Seat selection system

Movie search and filtering

Booking cancellation feature

Mobile responsive UI improvements

👩‍💻 Author

Sudha Chitral
