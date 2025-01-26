<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Webpage</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="logo">Logo</div>
        <nav>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="content">
            <div class="text-column">
                <h1>Welcome to Our Page</h1>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent libero. Sed cursus ante dapibus diam.</p>
            </div>
            <div class="image-column">
                <img src="https://via.placeholder.com/400" alt="Placeholder Image">
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Your Company. All Rights Reserved.</p>
        <ul class="social-links">
            <li><a href="#">Facebook</a></li>
            <li><a href="#">Twitter</a></li>
            <li><a href="#">Instagram</a></li>
        </ul>
    </footer>
</body>
</html>


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    background-color: #333;
    color: #fff;
}

header .logo {
    font-size: 1.5rem;
    font-weight: bold;
}

.nav-links {
    list-style: none;
    display: flex;
    gap: 15px;
}

.nav-links a {
    color: #fff;
    text-decoration: none;
    transition: color 0.3s;
}

.nav-links a:hover {
    color: #00bcd4;
}

main {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    padding: 20px;
}

.text-column {
    padding: 20px;
}

.image-column img {
    width: 100%;
    border-radius: 10px;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px 20px;
}

footer .social-links {
    list-style: none;
    display: flex;
    justify-content: center;
    gap: 15px;
    margin-top: 10px;
}

footer .social-links a {
    color: #00bcd4;
    text-decoration: none;
}

footer .social-links a:hover {
    color: #fff;
}

@media (max-width: 600px) {
    header {
        flex-direction: column;
        align-items: flex-start;
    }

    .nav-links {
        flex-direction: column;
        gap: 10px;
    }

    main {
        grid-template-columns: 1fr;
    }
}

@media (min-width: 601px) and (max-width: 1024px) {
    main {
        grid-template-columns: 1fr;
    }

    header, footer {
        flex-direction: row;
        justify-content: space-between;
    }
}

@media (min-width: 1025px) {
    main {
        grid-template-columns: 1fr 1fr;
    }
}

header, footer, .text-column, .image-column {
    transition: all 0.3s ease-in-out;
}
