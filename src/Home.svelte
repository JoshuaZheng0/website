<script>
    import Typing from './TypingAnimation.svelte';
</script>

<style>
    @keyframes slideInBottom {
    0% {
        transform: translateY(100%); /* Start from below the screen */
        opacity: 0; /* Start invisible */
    }
    100% {
        transform: translateY(0); /* End at original position */
        opacity: 1; /* End visible */
    }
    }

    @keyframes slideInLeft {
    0% {
        transform: translateX(-200%); /* Start off-screen */
        opacity: 0; /* Start invisible */
    }
    10% {
        opacity: 0; /* Remain invisible during the delay */
    }
    100% {
        transform: translateX(0); /* Slide to original position */
        opacity: 1; /* Fade in */
    }
	}

    @keyframes slideInRight {
    0% {
        transform: translateX(200%); /* Start off-screen */
        opacity: 0; /* Start invisible */
    }
    10% {
        opacity: 0; /* Remain invisible during the delay */
    }
    100% {
        transform: translateX(0); /* Slide to original position */
        opacity: 1; /* Fade in */
    }
	}

    header {
        animation: slideInBottom 1.5s ease forwards;
        background: linear-gradient(
            to right,
            #00A6ED,
            #cbaaf4
        );
        margin:1rem;
        color: #FFFFFF; /* Header text color */
        border-radius: 20px;
        text-align: center; /* Center header text */
    }

    .header-content {
        display: flex; /* Use flexbox for alignment */
        justify-content: space-between; /* Space between text and image */
        align-items: center; /* Center items vertically */
    }

    .header-text {
        margin-left: 2rem;
        animation: slideInright 1.5s ease forwards;
        text-align: left; /* Align text to the left */
    }

    .header-image {
        max-width: 20vw; /* Adjust width as needed */
        height: auto; /* Maintain aspect ratio */
        margin:.7rem; /* Space between text and image */
        border-radius: 20px;
    }
    a:hover .header-image {
        transform: scale(1.05); /* Slightly increase size on hover */
    }
    .image-link {
        text-align: center; /* Center the text within the link */
    }

    /* Mobile Styles */
@media only screen and (max-width: 600px) {
	:global(body) {
    overflow-x: hidden; /* Prevent horizontal scrolling */
	}
	header {
        background-color: #FF787A; /* Header background color */
        color: #FFFFFF; /* Header text color */
        border-radius: 20px;
    }
    .header-content {
        display: flex; /* Use flexbox for alignment */
        flex-direction: column;
        justify-content: space-between; /* Space between text and image */
        align-items: center; /* Center items vertically */
    }

    .header-text {
        text-align: left; /* Align text to the left */
    }

    .header-image {
        padding-top: 1rem;
        max-width: 90%; /* Adjust width as needed */
        height: auto; /* Maintain aspect ratio */
        margin: auto;
    }
}
</style>
<header>
    <div class="header-content">
        <a href="/assets/self-portrait-close.jpg" target="_blank" class="image-link">
            <img src="/assets/self-portrait-close.jpg" alt="Joshua Zheng holding Coffee" class="header-image" />
        </a>
        <div class="header-text">
            <h1><Typing/></h1>
            <h2>
                I'm a computer science undergraduate at the University of Maryland, 
                College Park, with experience in software development, web technologies, 
                and server management. I developed the ACM website and set up my own Debian server. 
                Beyond programming, I enjoy nature photography, running, and spending time with 
                my dog.     
            </h2>
            <br/>
            <br/>
            <h5 style="color: black">
                <a style="color: blue" href="https://github.com/JoshuaZheng0/website" target="_blank">This site</a> was made from scratch with Svelte and JavaScript—no templates! 🤣
            </h5>
        </div>
    </div>
</header>

