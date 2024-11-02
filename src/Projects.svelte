<script>
    import Project from './Project.svelte';

    const projects = [
        {
            title: 'ACM Website',
            image: '/assets/acm-website.jpg',
            description: 'As the Senior Web Developer for ACM@UMD, I developed the website (acm-umd.com) using Svelte. I integrated Google Analytics for traffic insights, implemented SEO strategies, and ensured a fully responsive design. Additionally, I managed continuous integration and deployment via Vercel, enhancing engagement.',
            github: 'https://github.com/acm-umd/umdwebsite',
            imagePosition: 'left',
            date: 'September 2024',
            languages: 'Svlete, Javascript, CSS, HTML',
            link: "https://www.acm-umd.com/"
        },
        {
            title: "Chicken Learn",
            image: "/assets/Chicken-learn.jpg",
            description: "Chicken Learn is an interactive web platform I created to make vocabulary building fun for children through 3D elements and animations. Built with Svelte and JavaScript, it features a user-friendly interface for exploring new words from the Random Word Generator API and definitions from DictionaryAPI. The platform includes dynamic visuals and custom CSS animations, all of which I designed without using templates.",
            github: "https://github.com/JoshuaZheng0/chicken-learn",
            imagePosition: "right",
            date: "October 2024",
            languages: "Svelte, JavaScript, CSS, HTML, Spline, DictionaryAPI",
            link: "https://chicken-learn.vercel.app/"
        },
        {
            title: 'Library Room Scraper',
            image: '/assets/library.jpg',
            description: 'The McKeldin Library at UMD is often crowded, making it hard for students to find available study rooms, so I created a Selenium Python script to automate room reservations, allowing users to secure study rooms up to a week in advance. This makes it easier for students to find available spaces.',
            github: 'https://github.com/JoshuaZheng0/library-reservation-scraper',
            imagePosition: 'left',
            date: 'September 2024',
            languages: 'Python, Selenium'
        },
        {
            title: 'Tesla Stock Price Predictor',
            image: '/assets/tesla.jpg',
            description: 'Developed an LSTM-based model to predict Tesla stock prices using Pandas, Numpy, and Keras. Integrated RSI indicators and evaluated performance with R-squared, max error, and variance metrics. Visualized prediction results with Matplotlib and web scraped data from Yahoo Finance using BeautifulSoup.',
            github: 'https://github.com/JoshuaZheng0/Tesla-Stock-Price-Prediction-Model',
            imagePosition: 'right',
            date: 'Summer 2023',
            languages: 'Python, Numpy, pandas, Plotly, BeautifulSoup'
        },
        {
            title: 'Drone Imaging and Interactive Tour Developer',
            image: '/assets/hl.jpg',
            description: 'Worked for the former Vice President of Warner Brothers to capture hundreds of aerial images with a drone and developed them into 360° photos using Photoshop. Created a 52-scene virtual walkthrough with Cloudpano and integrated the tour into a professional website.',
            github: 'https://github.com/yourusername/drone-imaging-interactive-tour',
            imagePosition: 'left',
            date: 'May 2024–August 2024',
            languages: 'Photography, Photoshop, Web Development',
            link: 'https://app.cloudpano.com/tours/nrUoBcJQb'
        },

        {
            title: 'C Compiler in Rust (In Progress)',
            image: '',
            description: 'Implemented a C compiler using Rust, focusing on performance and accuracy.',
            github: 'https://github.com/yourusername/c-compiler-rust',
            imagePosition: 'left',
            date: 'Aug 2024',
            languages: 'Rust'
        },
        {
            title: 'Brain-Controlled RC Car (In Progress)',
            image: '',
            description: 'A hat that allows control of an RC car using brain signals.',
            github: 'https://github.com/yourusername/brain-controlled-rc-car',
            imagePosition: 'left',
            date: 'Aug 2024',
            languages: 'Python, 3D Printing'
        },
        {
            title: 'Meme Generator App',
            image: '',
            description: 'Developed an Android app for creating memes using Java and Firebase for secure authentication and data synchronization. Utilized Firebase Storage and Base64 encoding for efficient image handling, and designed a responsive UI with dark/light mode while optimizing performance with dynamic content loading.',
            github: 'https://github.com/yourusername/meme-generator-app',
            imagePosition: 'left',
            date: 'Fall 2023',
            languages: 'Java, Firebase, Android Development, UI Design'
        },

        {
            title: 'Gambling Simulation Game',
            image: '',
            description: 'Created a 2D slots game featuring a graphical interface using Unity and C#. The game includes engaging gameplay mechanics and a user-friendly design.',
            github: 'https://github.com/yourusername/gambling-simulation-game',
            imagePosition: 'left',
            date: 'Spring 2024',
            languages: 'Unity, C#'
        },
    ];
</script>

<h1 class="projects-title">Projects</h1>
<div class="projects">
    {#each projects as project}
        <Project 
            title={project.title} 
            image={project.image} 
            description={project.description} 
            github={project.github} 
            imagePosition = {project.imagePosition}
            date = {project.date}
            languages = {project.languages}
            link = {project.link}
        />
    {/each}
</div>

<style>
    .projects-title {
        text-align: center;
        font-family: 'Quicksand', sans-serif;
        font-size: 3.5rem;
        margin-bottom: 20px; /* Optional: adds space below the title */
        color: #fff;
    }

    .projects {
        display: flex;
        flex-wrap: wrap;
        justify-content: center; /* Center projects within the container */
    }
</style>
