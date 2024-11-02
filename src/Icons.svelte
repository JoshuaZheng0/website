<script>
        let currentYear = new Date().getFullYear();
        export let onClick;
</script>


<nav>
    <a href="https://github.com/JoshuaZheng0/" target="_blank" class="icon-container">
        <img src="/assets/icons/github-mark-white.svg" alt="GitHub Icon" class="icon" />
    </a>
    <a href="https://www.linkedin.com/in/joshzheng7/" target="_blank" class="icon-container">
        <img src="/assets/icons/linkedin-icon-white.svg" alt="LinkedIn Icon" class="icon" />
    </a>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-missing-attribute -->
    <a on:click={onClick} class="icon-container">
        <img src="/assets/icons/email.png" alt="Terplink Icon" class="icon-terplink" />
    </a>
</nav>

<style>
    nav {
        padding-left: 20%;
        padding-right: 20%;
        margin: 20px;
        text-align: center;
    }

    nav a {
        margin: 10px;
        text-decoration: none;
        color: #FFD520; /* Nav link color */
        font-weight: bold;
        padding: 10px;
    }

    .icon, .icon-terplink {
        width: 40px; /* Set a fixed width */
        height: 40px; /* Set a fixed height */
        object-fit: contain; /* Ensures that the image scales correctly without distortion */
    }
    @media only screen and (max-width: 600px) {
        .icon {
        max-width: 8vw; /* Adjust the icon size */
        height: auto; /* Maintain aspect ratio */
        }
        .icon, .icon-terplink {
        width: 40px; /* Set a fixed width */
        height: 40px; /* Set a fixed height */
        object-fit: contain; /* Ensures that the image scales correctly without distortion */
    }
    .icon-container {
        display: flex;          /* Use flexbox to align items */
        align-items: center;   /* Center items vertically */
        justify-content: center; /* Center items horizontally */
        height: 100px;        /* Set a specific height for the container */
        margin-left: 1rem;    /* Set left margin */
        margin-right: 1rem;   /* Set right margin */
    }
    nav {
        display: flex; /* Enable flexbox */
        justify-content: center; /* Center items horizontally */
        padding: 10px;
    }

    nav a {
        margin: 10px; /* Space between links */
        text-decoration: none; /* Remove underline */
        color: #FFD520; /* Nav link color */
        font-weight: bold; /* Bold text */
    }
    }
</style>