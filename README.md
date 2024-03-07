<!DOCTYPE html>
<html lang="en">
<head>
<title>Vertical Navigation Menu</title>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {
  box-sizing: border-box;
  margin: 1;
  padding: 0;
}

body {
  font-family: Algerian;
}

/* Style the navigation container */
.navbar {
  background-color: #3223;
  width: 180px;
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
  color: black;
  text-decoration: none;
  transition: background-color 0.3s;
  
}

/* Change background color on hover */
.navbar a:hover {
  background-color: white;
  border-radius: 50%;
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

/* Show content based on target */
.content > div {
  display: none;
}

.content > div:target {
  display: block;
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
  <div id="home">
    <div class="header">
      <h1>Moseo De Filipinas</h1>
    </div>
    <div>
      <h2>Home</h2>
      <p>Our website is about a museum containing vast information in about phillipines</p>
    </div>
  </div>
  <div id="about">
    <div class="header">
      <h1>About Us</h1>
    </div>
    <div>
      <h2>About Us</h2>
      <p>This is the content of the About Us page.Information about our group.</p>
    </div>
  </div>
  <div id="references">
    <div class="header">
      <h1>References</h1>
    </div>
    <div>
      <h2>References</h2>
      <p>This is the content of the References page.Information and reference where we got the idea.</p>
    </div>
  </div>
  <div id="contact">
    <div class="header">
      <h1>Contact</h1>
    </div>
    <div>
      <h2>Contact</h2>
      <p>OUr personal information. Containing A little survey.</p>
    </div>
  </div>
</div>

</body>
</html>
