# zeditpvt.github.io


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Manish - Video Editor & Graphic Designer</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Header Section -->
    <header>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section id="hero">
        <h1>Hi, I'm Manish</h1>
        <p>Video Editor | Graphic Designer</p>
        <button>View Work</button>
    </section>

    <!-- About Section -->
    <section id="about">
        <h2>About Me</h2>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>My Projects</h2>
        <div class="project-grid">
            <!-- Add projects dynamically -->
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Get In Touch</h2>
        <form>
            <input type="text" placeholder="Name">
            <input type="email" placeholder="Email">
            <textarea placeholder="Message"></textarea>
            <button>Send</button>
        </form>
    </section>

    <script src="script.js"></script>
</body>
</html>


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body {
    line-height: 1.6;
}

header {
    background: #333;
    color: #fff;
    padding: 1em;
    text-align: center;
}

header nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-between;
}

header nav ul li {
    margin-right: 20px;
}

header nav a {
    color: #fff;
    text-decoration: none;
}

#hero {
    background-image: linear-gradient(to bottom, #333, #555);
    background-size: cover;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
}

.project-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
}


// Add event listener to view work button
document.querySelector('#hero button').addEventListener('click', () => {
    document.querySelector('#projects').scrollIntoView({ behavior: 'smooth' });
});

// Add projects dynamically
const projects = [
    { title: 'Project 1', image: 'project1.jpg' },
    { title: 'Project 2', image: 'project2.jpg' },
];

const projectGrid = document.querySelector('.project-grid');
projects.forEach((project) => {
    const projectHTML = `
        <div class="project">
            <img src="${project.image}" alt="${project.title}">
            <h3>${project.title}</h3>
        </div>
    `;
    projectGrid.innerHTML += projectHTML;
});
