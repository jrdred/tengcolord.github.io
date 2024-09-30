# tengcolord.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Welcome Page with Tabs">
    <title>Welcome to Jared's Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #4CAF50;
            color: white;
            padding: 15px;
            text-align: center;
        }
        .tab {
            display: flex;
            justify-content: center;
            background-color: #333;
        }
        .tab button {
            background-color: inherit;
            color: white;
            padding: 14px 20px;
            margin: 0;
            border: none;
            cursor: pointer;
            font-size: 16px;
            transition: background-color 0.3s;
        }
        .tab button:hover {
            background-color: #575757;
        }
        .tab button.active {
            background-color: #4CAF50;
        }
        .tab-content {
            display: none;
            padding: 20px;
            background-color: #fff;
            margin-top: 5px;
        }
        #about {
            display: block; /* Show the first tab by default */
        }
        footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

    <header>
        <h1>Welcome to Jared's Page</h1>
    </header>

    <div class="tab">
        <button class="tablinks" onclick="openTab(event, 'about')" id="defaultOpen">About Me</button>
        <button class="tablinks" onclick="openTab(event, 'socials')">Socials</button>
    </div>

    <div id="about" class="tab-content">
        <h2>About Me</h2>
        <p>Hi, I am <strong>Jared</strong>, a <strong>Master's Student in Biology</strong>. I am passionate about <strong>researching biological systems</strong> and love exploring new technologies and building creative solutions.</p>
    </div>

    <div id="socials" class="tab-content">
        <h2>Social Media</h2>
        <p>You can find me on:</p>
        <ul>
            <li><a href="https://www.instagram.com/jaweeeid/" target="_blank">Instagram</a></li>
            <!-- Add more social media links as needed -->
        </ul>
    </div>

    <footer>
        <p>&copy; 2024 Jared</p>
    </footer>

    <script>
        function openTab(evt, tabName) {
            var i, tabcontent, tablinks;
            
            // Hide all tab contents
            tabcontent = document.getElementsByClassName("tab-content");
            for (i = 0; i < tabcontent.length; i++) {
                tabcontent[i].style.display = "none";
            }
            
            // Remove the active class from all tabs
            tablinks = document.getElementsByClassName("tablinks");
            for (i = 0; i < tablinks.length; i++) {
                tablinks[i].className = tablinks[i].className.replace(" active", "");
            }
            
            // Show the selected tab
            document.getElementById(tabName).style.display = "block"; // Corrected here
            evt.currentTarget.className += " active";
        }

        // Default open tab
        document.getElementById("defaultOpen").click();
    </script>

</body>
</html>
