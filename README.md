<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Only Laughs - Stand-Up Comedy</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <!-- Side Navigation Bar -->
  <div class="sidenav" id="mySidenav">
    <h2>Only Laughs</h2>
    <a href="#old-school">Old School</a>
    <a href="#up-and-coming">Up & Coming</a>
    <a href="#weekly-top-picks">Weekly Top Picks</a>
    <a href="#new-releases">New Releases</a>
    <a href="#search">Search</a>
  </div>

  <!-- Main Content -->
  <div class="content">
    <h1>Welcome to Only Laughs</h1>
    <div id="old-school">
      <h2>Old School Comedians</h2>
      <div class="video-gallery">
        <div class="video-item">
          <img src="comedians/comic1.jpg" alt="Comic 1" class="thumbnail">
          <p>Comic 1 - Legendary Stand-Up</p>
        </div>
        <!-- Add more video items -->
      </div>
    </div>

    <div id="up-and-coming">
      <h2>Up & Coming Comedians</h2>
      <div class="video-gallery">
        <div class="video-item">
          <img src="comedians/comic2.jpg" alt="Comic 2" class="thumbnail">
          <p>Comic 2 - Rising Star</p>
        </div>
        <!-- Add more video items -->
      </div>
    </div>

    <div id="weekly-top-picks">
      <h2>Weekly Top Picks</h2>
      <div class="video-gallery">
        <div class="video-item">
          <img src="comedians/comic3.jpg" alt="Comic 3" class="thumbnail">
          <p>Comic 3 - Top of the Week</p>
        </div>
        <!-- Add more video items -->
      </div>
    </div>

    <div id="new-releases">
      <h2>New Releases</h2>
      <div class="video-gallery">
        <div class="video-item">
          <img src="comedians/comic4.jpg" alt="Comic 4" class="thumbnail">
          <p>Comic 4 - Latest Special</p>
        </div>
        <!-- Add more video items -->
      </div>
    </div>

    <div id="search">
      <h2>Search for Comedians</h2>
      <input type="text" id="search-input" placeholder="Search comedian...">
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
/* General Body and Layout */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  display: flex;
  background-color: #121212;  /* Dark background for contrast */
}

h1, h2 {
  color: #ffca28; /* Yellowish Gold for titles */
}

h2 {
  margin-top: 40px;
}

/* Side Navigation Bar */
.sidenav {
  height: 100%;
  width: 250px;
  position: fixed;
  top: 0;
  left: 0;
  background-color: #1f1f1f;
  padding-top: 20px;
  box-shadow: 2px 0px 10px rgba(0, 0, 0, 0.1);
}

.sidenav h2 {
  text-align: center;
  color: #ffca28;
  margin-bottom: 20px;
}

.sidenav a {
  padding: 10px 15px;
  text-decoration: none;
  font-size: 18px;
  color: white;
  display: block;
  transition: background-color 0.3s ease;
}

.sidenav a:hover {
  background-color: #ffca28;
  color: #1f1f1f;
}

/* Main Content */
.content {
  margin-left: 250px;
  padding: 20px;
  color: white;
  width: 100%;
}

.video-gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  margin-top: 20px;
}

.video-item {
  background-color: #333;
  border-radius: 8px;
  overflow: hidden;
  width: 180px;
}

.video-item img {
  width: 100%;
  height: auto;
}

.thumbnail {
  border-radius: 8px;
}

.video-item p {
  padding: 10px;
  font-size: 14px;
  text-align: center;
}

/* Search Section */
#search {
  margin-top: 40px;
}

#search input {
  padding: 10px;
  width: 300px;
  border-radius: 5px;
  border: none;
  font-size: 16px;
}

/* Page Breaks */
@media print {
  .video-gallery {
    page-break-before: always;
  }
}
document.getElementById('search-input').addEventListener('input', function() {
  let searchTerm = this.value.toLowerCase();
  let videos = document.querySelectorAll('.video-item p');

  videos.forEach(function(video) {
    let text = video.innerText.toLowerCase();
    if (text.includes(searchTerm)) {
      video.parentElement.style.display = 'block';
    } else {
      video.parentElement.style.display = 'none';
    }
  });
});
