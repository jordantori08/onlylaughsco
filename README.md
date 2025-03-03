<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OnlyLaughs - Stand-Up Comedy</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Welcome to OnlyLaughs</h1>
        <p>Your go-to platform for stand-up comedy shows!</p>
    </header>
    
    <div class="video-container">
        <div class="video-card">
            <h2>Comedy Show 1</h2>
            <video width="100%" controls>
                <source src="comedy_show_1.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </div>
        
        <div class="video-card">
            <h2>Comedy Show 2</h2>
            <video width="100%" controls>
                <source src="comedy_show_2.mp4" type="video/mp4">
                Your browser does not support the video tag.
            </video>
        </div>
    </div>

    <footer>
        <p>&copy; 2025 OnlyLaughs.co</p>
    </footer>
</body>
</html>
document.addEventListener("DOMContentLoaded", function() {
    // Future JavaScript functions to enhance interactivity
});
/* Global Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

header {
    background-color: #222;
    color: white;
    text-align: center;
    padding: 20px;
}

h1 {
    margin: 0;
    font-size: 2.5em;
}

.video-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    padding: 20px;
}

.video-card {
    background: white;
    border-radius: 10px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    width: 45%;
    margin: 10px;
    padding: 15px;
    text-align: center;
}

footer {
    background-color: #222;
    color: white;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
}
