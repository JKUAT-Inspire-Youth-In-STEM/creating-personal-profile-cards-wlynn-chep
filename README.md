<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Profile Card</title>
    <style>
        /* General page styling */
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh; /* Makes sure the content is centered on the full screen */
            background-color: #f4f4f4;
            transition: background 0.3s; /* Smooth transition when switching themes */
        }
        
        /* Profile card styling */
        .card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 300px;
            transition: background 0.3s, color 0.3s; /* Smooth transition for theme change */
        }
        
        /* Profile image styling */
        .card img {
            width: 100px;
            height: 100px;
            border-radius: 50%; /* Makes the image circular */
        }
        
        /* Smooth text color transition */
        .card h2, .card p {
            transition: color 0.3s;
        }
        
        /* Button styling */
        .btn {
            background: blue;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            margin: 5px;
        }
        
        /* Dark mode styles */
        .dark-mode {
            background-color: #333;
            color: white;
        }
    </style>
</head>
<body>
    <!-- Profile Card -->
    <div class="card" id="profile-card">
        <img src="https://via.placeholder.com/100" alt="Profile Picture"> <!-- Placeholder profile image -->
        <h2 id="name">John Doe</h2> <!-- Default name -->
        <p id="bio">Web Developer & Designer</p> <!-- Default bio -->
        
        <!-- Buttons to edit profile and toggle dark mode -->
        <button class="btn" onclick="editProfile()">Edit Profile</button>
        <button class="btn" onclick="toggleTheme()">Toggle Theme</button>
    </div>

    <script>
        /* Function to edit the profile details */
        function editProfile() {
            // Prompt user for a new name and bio
            let newName = prompt("Enter new name:", document.getElementById('name').textContent);
            let newBio = prompt("Enter new bio:", document.getElementById('bio').textContent);
            
            // Update the profile only if the user enters new values
            if (newName) document.getElementById('name').textContent = newName;
            if (newBio) document.getElementById('bio').textContent = newBio;
        }
        
        /* Function to toggle between light and dark mode */
        function toggleTheme() {
            document.body.classList.toggle("dark-mode"); // Apply dark mode to the entire page
            document.getElementById("profile-card").classList.toggle("dark-mode"); // Apply dark mode to the card
        }
    </script>
</body>
</html>
