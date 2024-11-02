<script>
    import Home from './Home.svelte';
    import Contact from './Contact.svelte';
    import Leadership from './Leadership.svelte';
    import Projects from './Projects.svelte';
    import Icons from './Icons.svelte';

   
    let currentYear = new Date().getFullYear();
    
    // References for scrolling
    let homeRef;
    let projectsRef;
    let contactRef;

    function navigate(ref) {
        if (ref) {
            ref.scrollIntoView({ behavior: 'smooth' }); // Scroll to the referenced element
        }
    }
</script>

<style>
    @keyframes slideInRight {
        0% {
            transform: translateX(200%);
            opacity: 0;
        }
        100% {
            transform: translateX(0);
            opacity: 1;
        }
    }

    @keyframes slideInLeft {
        0% {
            transform: translateX(-200%);
            opacity: 0;
        }
        100% {
            transform: translateX(0);
            opacity: 1;
        }
    }
	
    :global(body) {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
        margin: 0;
        background-color: #080b0d;
    }
    nav {
        display: flex;
        justify-content: space-between; /* Aligns logo to the left and buttons to the right */
        align-items: center; /* Centers items vertically */
        margin: auto;
    }

    .content {
        margin-top: 10px;
    }

    footer {
        margin-top: 40px;
        text-align: center;
        padding: 10px;
        background: linear-gradient(
        to bottom,
        #E9F1F7,
        #008BF8     
        );
        color: #FFFFFF; /* Footer text color */
        border-top-left-radius: 20px; /* Adjust the value as needed */
        border-top-right-radius: 20px; /* Adjust the value as needed */
    }

    footer a {
        color: #FFD520; /* Footer link color */
        margin: 10px;
        text-decoration: none;
        font-weight: bold;
    }


    .icon, .icon-terplink {
        width: 40px; /* Set a fixed width */
        height: 40px; /* Set a fixed height */
        object-fit: contain; /* Ensures that the image scales correctly without distortion */
    }

    .button {
        animation: slideInRight 1.5s ease forwards;
        margin-left: 2rem; /* Change from 2vw to 2rem */
        cursor: pointer;
        text-decoration: none;
        color: #008BF8;
        background: none;
        border: none;
        font-size: 2.5rem; /* Adjust the font size as needed */
        outline: none;
        font-family: 'Quicksand', sans-serif;
        font-weight: bold; 
    }


    .button:hover {
        text-decoration: underline;
    }

    .button:focus {
        background: none;
        outline: none;
    }

    .content {
        flex: 1; /* Allow the content area to grow and take available space */
    }
	footer a {
        color: #FFD520; /* Footer link color */   
    }

    @media only screen and (max-width: 600px) {
        .button {
            animation: slideInRight 1.5s ease forwards;
            margin-left: .1rem; /* Change from 2vw to 2rem */
            cursor: pointer;
            text-decoration: none;
            color: #008BF8;
            background: none;
            border: none;
            font-size: 1.4rem; /* Adjust the font size as needed */
            outline: none;
            font-family: 'Quicksand', sans-serif;
            font-weight: bold; 
        }
    }
</style>

<nav>
    <div style="justify-content: center;">
        <button class="button" on:click={() => navigate(homeRef)}>About Me</button>
        <button class="button" on:click={() => navigate(projectsRef)}>Projects</button>
        <button class="button" on:click={() => navigate(contactRef)}>Contact</button>
    </div>
</nav>

<div class="content">
    <div bind:this={homeRef}><Home /></div>
    <Icons  onClick={() => navigate(contactRef)}/>
    <Leadership/>
    <div bind:this={projectsRef}><Projects/></div>
    <div bind:this={contactRef}><Contact/></div>
</div>

<footer>
    <p>&copy;{currentYear}</p>

        <a href="https://github.com/JoshuaZheng0/" target="_blank" class="icon-container">
            <img src="/assets/icons/github-mark-white.svg" alt="GitHub Icon" class="icon" />
        </a>
        <a href="https://www.linkedin.com/in/joshzheng7/" target="_blank" class="icon-container">
            <img src="/assets/icons/linkedin-icon-white.svg" alt="LinkedIn Icon" class="icon" />
        </a>
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <!-- svelte-ignore a11y-missing-attribute -->
        <a on:click={() => navigate(contactRef)} class="icon-container">
            <img src="/assets/icons/email.png" alt="Terplink Icon" class="icon-terplink" />
        </a>
</footer>

