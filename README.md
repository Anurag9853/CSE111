# CSE111
website
<br>
author-Anurag
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: url('your-background-image.jpg') center/cover no-repeat; /* Add your background image */
            color: #333;
        }

        header {
            background-color: #4CAF50;
            color: white;
            text-align: center;
            padding: 1em;
        }

        h1 {
            margin: 0;
            font-size: 2em; /* Increased font size */
            font-weight: bold;
            color: black; /* Black title color */
        }

        nav {
            text-align: center;
            margin-top: 1em;
        }

        nav a {
            display: inline-block;
            margin: 0.5em;
            padding: 0.5em 1em;
            color: white;
            text-decoration: none;
            background-color: #55acee; /* Blue background color for buttons */
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        nav a:hover {
            background-color: #357ebd; /* Darker blue on hover */
        }

        .signup-button {
            background-color: #e74c3c; /* Red background color for Sign Up button */
            cursor: pointer;
        }

        .signup-form {
            display: none;
            text-align: center;
            background-color: #fff;
            padding: 1em;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        section {
            max-width: 800px;
            margin: 2em auto;
            padding: 1em;
            background-color: #fff;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        section form {
            background-color: #e0f7fa; /* Light green background color for the form section */
            padding: 1em;
            border-radius: 8px;
        }

        details {
            margin-bottom: 1em;
        }

        details summary {
            cursor: pointer;
            font-weight: bold;
            padding: 0.3em 0.5em; /* Reduced padding */
            background-color: #ddd;
            border: 1px solid #ccc;
            border-radius: 4px;
            position: relative;
            z-index: 1;
        }

        details p {
            margin: 0;
            padding: 0.5em;
            border: 1px solid #ccc;
            border-radius: 4px;
            background-color: #f9f9f9;
            position: relative;
            z-index: 0;
        }

        details:hover p {
            display: block;
        }

        label {
            display: block;
            margin-bottom: 0.5em;
            color: #555;
        }

        input, select, textarea {
            width: 100%;
            padding: 0.5em;
            margin-bottom: 1em;
            border: 1px solid #ccc;
            border-radius: 4px;
            box-sizing: border-box;
        }

        button {
            background-color: #4CAF50;
            color: white;
            padding: 0.5em 1em;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        #confirmationMessage {
            margin-top: 1em;
            font-weight: bold;
            color: #4CAF50;
        }

        .contact-info {
            text-align: center;
            margin-top: 1em;
            font-weight: bold;
        }
        
        /* Style for the dropdown menu */
        .dropdown {
            position: relative;
            display: inline-block;
        }

        .dropdown-content {
            display: none;
            position: absolute;
            background-color: #f9f9f9;
            min-width: 160px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
            z-index: 1;
        }

        .dropdown:hover .dropdown-content {
            display: block;
        }

    </style>
    <title>Pet Sitting and Pet Care Services</title>
</head>
<body>
    <header>
        <h1>Pet Sitting and Pet Care Services</h1>
    </header>

    <nav>
        <a href="#" onclick="displayHomeMessage()">Home <i class="fas fa-home"></i></a>
        <details>
            <summary>About Us <i class="fas fa-info-circle"></i></summary>
            <p>Our mission is to provide high-quality and compassionate care for your pets. We strive to create a positive and safe environment for your furry friends.</p>
            <p>Meet our dedicated team:</p>
            <ul>
                <li>Anurag</li>
                <li>Aryan</li>
                <li>Thaghat</li>
                <!-- Add more team members as needed -->
            </ul>
        </details>
        <!-- Add the dropdown menu under "Contact Us" -->
        <div class="dropdown">
            <a href="#" class="contact-button">Contact Us <i class="fas fa-envelope"></i></a>
            <div class="dropdown-content">
                <p>Email: <a href="mailto:petcare@gmail.com">petcare@gmail.com</a></p>
            </div>
        </div>
        <div class="signup-button" onclick="toggleSignupForm()">Sign Up <i class="fas fa-user-plus"></i></div>
    </nav>

    <div class="signup-form" id="signupForm">
        <h2>Sign Up</h2>
        <!-- Add your signup form fields here -->
        <label for="username">Username:</label>
        <input type="text" id="username" name="username" required>

        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>

        <button type="button" onclick="submitSignupForm()">Submit</button>
    </div>

    <section>
        <h2>Our Services</h2>
        <p>We offer professional pet sitting and care services. Fill out the form below to book our services.</p>

        <form id="bookingForm">
            <label for="petName">Pet Name:</label>
            <input type="text" id="petName" name="petName" required>

            <label for="serviceType">Service Type:</label>
            <select id="serviceType" name="serviceType" required>
                <option value="petSitting">Pet Sitting</option>
                <option value="dogWalking">Dog Walking</option>
                <option value="feeding">Feeding</option>
            </select>

            <label for="date">Date:</label>
            <input type="date" id="date" name="date" required>

            <label for="additionalInfo">Additional Information:</label>
            <textarea id="additionalInfo" name="additionalInfo" rows="4"></textarea>

            <button type="button" onclick="submitForm()">Submit</button>
        </form>

        <div id="confirmationMessage"></div>
    </section>

    <section class="contact-info">
        <h2>Contact Us</h2>
        <p>For inquiries, please contact us at: <br> <a href="tel:+18575757747">857-575-7747</a></p>
    </section>

    <script>
        function toggleSignupForm() {
            var signupForm = document.getElementById("signupForm");
            signupForm.style.display = (signupForm.style.display === "none" || signupForm.style.display === "") ? "block" : "none";
        }

        function submitSignupForm() {
            // Add logic to handle signup form submission
            // You can use AJAX or other techniques to send data to the server
            alert("Signup form submitted!");
        }

        function submitForm() {
            // Get form values
            var petName = document.getElementById("petName").value;
            var serviceType = document.getElementById("serviceType").value;
            var date = document.getElementById("date").value;
            var additionalInfo = document.getElementById("additionalInfo").value;

            // Basic form validation
            if (!petName || !serviceType || !date) {
                alert("Please fill out all required fields.");
                return;
            }

            // Create a confirmation message
            var confirmationMessage = `Thank you, ${petName}! You have successfully booked ${serviceType} for ${date}.`;

            // Display the confirmation message
            document.getElementById("confirmationMessage").innerText = confirmationMessage;

            // Optionally, you can send the form data to a server using AJAX or fetch for further processing.
        }

        function displayHomeMessage() {
            alert("You are on the Home page!");
        }
    </script>
</body>
</html>

