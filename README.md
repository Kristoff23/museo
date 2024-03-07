<!DOCTYPE html>
<html lang="en">
<head>
<title>Vertical Navigation Menu</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, sans-serif;
}

/* Style the navigation container */
.navbar {
  background-color: #333;
  width: 200px;
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  padding-top: 20px;
}

/* Style the navigation links */
.navbar a {
  display: block;
  padding: 10px 20px;
  color: white;
  text-decoration: none;
  transition: background-color 0.3s;
}

/* Change background color on hover */
.navbar a:hover {
  background-color: #555;
  border-radius: 50%;
}

/* Add animation */
.navbar a:hover::before {
  content: '';
  position: absolute;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background-color: #555;
  animation: pulse 0.5s infinite alternate;
}

/* Keyframe animation */
@keyframes pulse {
  0% {
    transform: scale(1);
    opacity: 0.7;
  }
  100% {
    transform: scale(1.5);
    opacity: 0;
  }
}

/* Style the content */
.content {
  margin-left: 220px; /* Adjusted to accommodate the width of the navbar */
  padding: 20px;
}

/* Style the header */
.header {
  background-color: #f1f1f1;
  padding: 20px;
  text-align: center;
}
</style>
</head>
<body>

<div class="navbar">
  <a href="#home">Home</a>
  <a href="#about">About Us</a>
  <a href="#references">References</a>
  <a href="#contact">Contact</a>
</div>

<div class="content">
  <div class="header">
    <h1>Welcome to Our Website</h1>
  </div>
  <p>This is the content of the website. Replace this text with your actual content.</p>
</div>

</body>
</html>
