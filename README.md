<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OnlyLaughs - Stand-Up Comedy</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Side Navigation Bar -->
    <div class="sidenav">
        <h2>OnlyLaughs</h2>
        <a href="#" class="active">Home</a>
        <a href="#comedy">Comedy Shows</a>
        <a href="#search">Search</a>
    </div>

    <!-- Main Content -->
    <div class="main-content">
        <!-- Search Bar -->
        <div class="search-container" id="search">
            <input type="text" id="searchInput" placeholder="Search for comedy shows..." onkeyup="searchVideos()">
        </div>

        <!-- Video Thumbnails -->
        <section id="comedy" class="video-container">
            <div class="video-card" data-title="Comedy Show 1">
                <img src="thumb1.jpg" alt="Comedy Show 1" class="video-thumbnail">
                <div class="video-info">
                    <h3>Comedy Show 1</h3>
                    <p>Stand-up comedy special from comedian 1.</p>
                </div>
            </div>

            <div class="video-card" data-title="Comedy Show 2">
                <img src="thumb2.jpg" alt="Comedy Show 2" class="video-thumbnail">
                <div class="video-info">
                    <h3>Comedy Show 2</h3>
                    <p>A hilarious set by comedian 2, covering family life.</p>
                </div>
            </div>

            <div class="video-card" data-title="Comedy Show 3">
                <img src="thumb3.jpg" alt="Comedy Show 3" class="video-thumbnail">
                <div class="video-info">
                    <h3>Comedy Show 3</h3>
                    <p>Comedian 3 shares stories about life on the road.</p>
                </div>
            </div>

            <div class="video-card" data-title="Comedy Show 4">
                <img src="thumb4.jpg" alt="Comedy Show 4" class="video-thumbnail">
                <div class="video-info">
                    <h3>Comedy Show 4</h3>
                    <p>Stand-up special from comedian 4 featuring political humor.</p>
                </div>
            </div>

            <!-- Add more video cards as needed -->
        </section>
    </div>

    <footer>
        <p>&copy; 2025 OnlyLaughs.co</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
/* Global Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    height: 100vh;
    background-color: #141414;
    color: white;
}

.sidenav {
    height: 100%;
    width: 250px;
    position: fixed;
    top: 0;
    left: 0;
    background-color: #222;
    padding-top: 20px;
    color: white;
    text-align: center;
}

.sidenav h2 {
    font-size: 2em;
    color: #ff4b2b;
}

.sidenav a {
    padding: 15px;
    text-decoration: none;
    font-size: 1.2em;
    color: white;
    display: block;
    border-bottom: 1px solid #444;
}

.sidenav a:hover, .sidenav .active {
    background-color: #ff4b2b;
}

.main-content {
    margin-left: 250px;
    padding: 20px;
    flex-grow: 1;
}

.search-container {
    margin-bottom: 30px;
}

#searchInput {
    width: 100%;
    padding: 10px;
    font-size: 1.1em;
    border: 2px solid #555;
    border-radius: 5px;
    background-color: #333;
    color: white;
    margin-bottom: 20px;
}

.video-container {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}

.video-card {
    width: 220px;
    background: #333;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
    text-align: center;
    transition: transform 0.3s ease;
}

.video-card:hover {
    transform: scale(1.05);
}

.video-thumbnail {
    width: 100%;
    height: 120px;
    object-fit: cover;
    border-bottom: 3px solid #ff4b2b;
}

.video-info {
    padding: 10px;
}

h3 {
    font-size: 1.3em;
    margin: 10px 0;
}

footer {
    text-align: center;
    color: #999;
    padding: 20px 0;
    background-color: #222;
    position: absolute;
    bottom: 0;
    width: 100%;
}
// Search functionality to filter videos based on title
function searchVideos() {
    const query = document.getElementById('searchInput').value.toLowerCase();
    const videoCards = document.querySelectorAll('.video-card');
    
    videoCards.forEach(card => {
        const title = card.getAttribute('data-title').toLowerCase();
        if (title.includes(query)) {
            card.style.display = 'block';
        } else {
            card.style.display = 'none';
        }
    });
}
