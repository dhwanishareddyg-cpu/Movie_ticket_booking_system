# Movie_ticket_booking_system
An online movie ticket system in Java is a project that allows us to view movies, we can also search for showtimes, and book tickets. This project helps beginners to learn core concepts like object-oriented programming, collections, and user-input handling as well.

Project Title:

Movie Ticket Booking System


Project Description:
The Movie Ticket Booking System is a Java-based application developed to automate the process of booking movie tickets. This system allows users to view available movies, select show timings, book tickets, and manage booking details efficiently.
The project is designed using Java concepts such as classes, objects, inheritance, exception handling, collections, file handling, and JDBC for database connectivity. It provides a simple and user-friendly interface for managing movie ticket reservations.


Features:
User registration and login
Display available movies
Show movie timings and seat availability
Book movie tickets
Cancel booked tickets
Generate booking details and receipt
Admin can add/update/delete movie details
Database connectivity using JDBC
Simple and interactive user interface


Software Requirements:

Hardware Requirements
Processor: Intel i3 or above
RAM: 4 GB minimum
Storage: 500 MB free space


Software Requirements
Operating System: Windows/Linux/Mac
Java Development Kit (JDK 8 or above)
NetBeans / Eclipse / IntelliJ IDEA
MySQL Database
JDBC Driver
Command Prompt or Terminal


Steps to Run the Project:

Step 1: Install Required Software
Install Java JDK
Install MySQL Database
Install any Java IDE (NetBeans/Eclipse/IntelliJ)


Step 2: Create Database
Open MySQL.
Create a database named:
SQL
CREATE DATABASE movie_booking;
Create required tables for users, movies, bookings, etc.


Step 3: Configure JDBC
Add MySQL JDBC Driver to the project libraries.
Update database username and password in the Java code.
Example:
Java
String url = "jdbc:mysql://localhost:3306/movie_booking";
String user = "root";
String password = "your_password";


Step 4: Compile the Project
Using terminal:
Bash
javac Main.java


Step 5: Run the Project
Using terminal:
Bash
java Main
Or run directly using the IDE.



HTML code:


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CineBook - Movie Ticket Booking System</title>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">

    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- NAVIGATION -->
    <nav>
        <a href="#" class="nav-logo">🎬 <span>CineBook</span></a>

        <ul class="nav-links">
            <li><a href="#hero">Home</a></li>
            <li><a href="#movies">Movies</a></li>
            <li><a href="#booking">Book Tickets</a></li>
            <li><a href="#reports">Reports</a></li>
        </ul>

        <div class="nav-actions">
            <button class="btn-nav btn-ghost">Login</button>
            <button class="btn-nav btn-gold">Register</button>
        </div>
    </nav>

    <!-- HERO SECTION -->
    <section id="hero">
        <div class="hero-bg"></div>
        <div class="hero-grid"></div>

        <div class="hero-content">
            <div class="hero-badge">Premium Cinema Experience</div>

            <h1 class="hero-title">
                Book Your <em>Movie Tickets</em> in Seconds
            </h1>

            <p class="hero-sub">
                Explore the latest blockbusters, choose your seats, and enjoy a premium movie experience with CineBook.
            </p>

            <div class="hero-actions">
                <button class="btn-primary">Book Now</button>
                <button class="btn-outline">View Movies</button>
            </div>

            <div class="hero-stats">
                <div class="stat-item">
                    <div class="stat-num">50+</div>
                    <div class="stat-label">Movies</div>
                </div>

                <div class="stat-item">
                    <div class="stat-num">100K+</div>
                    <div class="stat-label">Bookings</div>
                </div>

                <div class="stat-item">
                    <div class="stat-num">20+</div>
                    <div class="stat-label">Cities</div>
                </div>
            </div>
        </div>
    </section>

    <!-- MOVIES SECTION -->
    <section id="movies">
        <div class="section-label">Now Showing</div>
        <h2 class="section-title">Choose Your Movie</h2>
        <p class="section-sub">Select from the latest trending blockbusters.</p>

        <div class="movies-grid">

            <div class="movie-card">
                <div class="movie-poster">🎥</div>
                <div class="movie-info">
                    <h3>Avengers Endgame</h3>
                    <div class="movie-meta">
                        <span>Action</span>
                        <span>⭐ 9.2</span>
                    </div>
                </div>
            </div>

            <div class="movie-card">
                <div class="movie-poster">🚀</div>
                <div class="movie-info">
                    <h3>Interstellar</h3>
                    <div class="movie-meta">
                        <span>Sci-Fi</span>
                        <span>⭐ 9.0</span>
                    </div>
                </div>
            </div>

            <div class="movie-card">
                <div class="movie-poster">👻</div>
                <div class="movie-info">
                    <h3>The Conjuring</h3>
                    <div class="movie-meta">
                        <span>Horror</span>
                        <span>⭐ 8.7</span>
                    </div>
                </div>
            </div>

        </div>
    </section>

    <!-- BOOKING SECTION -->
    <section id="booking">
        <div class="section-label">Book Tickets</div>
        <h2 class="section-title">Select Your Seats</h2>

        <div class="booking-layout">

            <!-- Seat Layout -->
            <div class="seat-section">
                <div class="screen-wrap">
                    <div class="screen-bar"></div>
                    <div class="screen-label">SCREEN</div>
                </div>

                <div class="seat-grid" id="seatGrid">
                    <!-- Seats generated by JS -->
                </div>
            </div>

            <!-- Booking Panel -->
            <div class="booking-panel">
                <h3>Booking Summary</h3>

                <div class="panel-field">
                    <label>Movie</label>
                    <select id="movieSelect">
                        <option>Avengers Endgame</option>
                        <option>Interstellar</option>
                        <option>The Conjuring</option>
                    </select>
                </div>

                <div class="panel-field">
                    <label>Name</label>
                    <input type="text" placeholder="Enter your name">
                </div>

                <div class="selected-seats-display" id="selectedSeats">
                    No seats selected
                </div>

                <div class="price-total">
                    <span>Total</span>
                    <span class="amount" id="totalPrice">₹0</span>
                </div>

                <button class="btn-book" id="bookBtn">Confirm Booking</button>
            </div>

        </div>
    </section>

    <!-- REPORT SECTION -->
    <section id="reports">
        <div class="section-label">Reports</div>
        <h2 class="section-title">Booking Analytics</h2>

        <div class="reports-grid">
            <div class="report-card">
                <div class="r-label">Total Bookings</div>
                <div class="r-value">15,240</div>
            </div>

            <div class="report-card">
                <div class="r-label">Revenue</div>
                <div class="r-value gold">₹8.2L</div>
            </div>

            <div class="report-card">
                <div class="r-label">Movies Running</div>
                <div class="r-value">52</div>
            </div>

            <div class="report-card">
                <div class="r-label">Occupancy</div>
                <div class="r-value">89%</div>
            </div>
        </div>
    </section>

    <script src="script.js"></script>

</body>
</html>


CSS code:


/* Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body {
    background: #0f0f1a;
    color: white;
    line-height: 1.6;
}

/* Header */
header {
    background: linear-gradient(90deg, #111, #1a1a2e);
    padding: 15px 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: sticky;
    top: 0;
    z-index: 1000;
}

header .logo {
    font-size: 28px;
    font-weight: bold;
    color: #ff4d6d;
}

header nav ul {
    display: flex;
    list-style: none;
    gap: 25px;
}

header nav ul li a {
    text-decoration: none;
    color: white;
    transition: 0.3s;
}

header nav ul li a:hover {
    color: #ff4d6d;
}

/* Hero Section */
.hero {
    height: 90vh;
    background: url('https://images.unsplash.com/photo-1524985069026-dd778a71c7b4')
        no-repeat center center/cover;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
}

.hero-content {
    background: rgba(0, 0, 0, 0.6);
    padding: 40px;
    border-radius: 15px;
}

.hero-content h1 {
    font-size: 50px;
    margin-bottom: 20px;
}

.hero-content p {
    font-size: 20px;
    margin-bottom: 20px;
}

.btn {
    background: #ff4d6d;
    color: white;
    padding: 12px 25px;
    text-decoration: none;
    border-radius: 8px;
    transition: 0.3s;
}

.btn:hover {
    background: #ff1e4d;
}

/* Movies Section */
.movies {
    padding: 60px 50px;
    text-align: center;
}

.movies h2 {
    margin-bottom: 30px;
    font-size: 36px;
}

.movie-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 25px;
}

.movie-card {
    background: #1a1a2e;
    border-radius: 15px;
    overflow: hidden;
    transition: transform 0.3s;
}

.movie-card:hover {
    transform: translateY(-10px);
}

.movie-card img {
    width: 100%;
    height: 350px;
    object-fit: cover;
}

.movie-card h3 {
    margin: 15px 0;
}

.movie-card p {
    padding: 0 15px 20px;
    font-size: 14px;
}

/* Booking Form */
.booking {
    padding: 60px 50px;
    background: #111;
    text-align: center;
}

.booking h2 {
    margin-bottom: 30px;
    font-size: 36px;
}

.booking form {
    max-width: 500px;
    margin: auto;
    display: flex;
    flex-direction: column;
    gap: 15px;
}

.booking input,
.booking select,
.booking button {
    padding: 12px;
    border: none;
    border-radius: 8px;
    outline: none;
}

.booking button {
    background: #ff4d6d;
    color: white;
    cursor: pointer;
    transition: 0.3s;
}

.booking button:hover {
    background: #ff1e4d;
}

/* Footer */
footer {
    background: #1a1a2e;
    text-align: center;
    padding: 20px;
    margin-top: 40px;
}

/* Responsive */
@media (max-width: 768px) {
    header {
        flex-direction: column;
        padding: 20px;
    }

    header nav ul {
        flex-direction: column;
        text-align: center;
        gap: 15px;
    }

    .hero-content h1 {
        font-size: 35px;
    }

    .hero-content p {
        font-size: 16px;
    }
}



JavaScript:



// Wait until page loads
document.addEventListener("DOMContentLoaded", () => {

    // ==========================
    // Booking Form Functionality
    // ==========================
    const bookingForm = document.getElementById("bookingForm");

    if (bookingForm) {
        bookingForm.addEventListener("submit", function (e) {
            e.preventDefault();

            const name = document.getElementById("name").value.trim();
            const movie = document.getElementById("movie").value;
            const seats = document.getElementById("seats").value;
            const date = document.getElementById("date").value;

            if (name === "" || movie === "" || seats === "" || date === "") {
                alert("⚠️ Please fill in all booking details!");
                return;
            }

            alert(
                `🎉 Booking Confirmed!\n\n` +
                `Name: ${name}\n` +
                `Movie: ${movie}\n` +
                `Seats: ${seats}\n` +
                `Date: ${date}`
            );

            bookingForm.reset();
        });
    }

    // ==========================
    // Seat Selection Functionality
    // ==========================
    const seatContainer = document.getElementById("seatContainer");
    const selectedSeatsDisplay = document.getElementById("selectedSeats");
    const totalPriceDisplay = document.getElementById("totalPrice");

    let selectedSeats = [];
    const seatPrice = 10; // Price per seat

    if (seatContainer) {
        // Generate seats dynamically
        for (let i = 1; i <= 30; i++) {
            const seat = document.createElement("div");
            seat.classList.add("seat");
            seat.textContent = i;

            // Randomly mark some seats as booked
            if (Math.random() < 0.2) {
                seat.classList.add("booked");
            }

            seat.addEventListener("click", () => {
                if (seat.classList.contains("booked")) {
                    alert("❌ This seat is already booked!");
                    return;
                }

                seat.classList.toggle("selected");

                const seatNumber = seat.textContent;

                if (seat.classList.contains("selected")) {
                    selectedSeats.push(seatNumber);
                } else {
                    selectedSeats = selectedSeats.filter(
                        seatNum => seatNum !== seatNumber
                    );
                }

                updateSeatInfo();
            });

            seatContainer.appendChild(seat);
        }
    }

    // Update selected seats info
    function updateSeatInfo() {
        if (selectedSeatsDisplay) {
            selectedSeatsDisplay.textContent =
                selectedSeats.length > 0
                    ? selectedSeats.join(", ")
                    : "None";
        }

        if (totalPriceDisplay) {
            totalPriceDisplay.textContent =
                `$${selectedSeats.length * seatPrice}`;
        }
    }

    // ==========================
    // Movie Card Button Alerts
    // ==========================
    const movieButtons = document.querySelectorAll(".movie-card .btn");

    movieButtons.forEach(button => {
        button.addEventListener("click", () => {
            const movieName = button.parentElement.querySelector("h3").textContent;
            alert(`🎬 You selected "${movieName}"! Scroll down to book tickets.`);
        });
    });

    // ==========================
    // Smooth Scroll for Nav Links
    // ==========================
    const navLinks = document.querySelectorAll("nav a");

    navLinks.forEach(link => {
        link.addEventListener("click", function (e) {
            const targetId = this.getAttribute("href");

            if (targetId.startsWith("#")) {
                e.preventDefault();

                const targetSection = document.querySelector(targetId);

                if (targetSection) {
                    targetSection.scrollIntoView({
                        behavior: "smooth"
                    });
                }
            }
        });
    });

});
