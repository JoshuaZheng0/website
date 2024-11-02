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
        padding: 10px;
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
        margin-left: 20px; /* Space between text and image */
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
        padding: 10px;
        color: #FFFFFF; /* Header text color */
        border-radius: 20px;
    }
    .header-content {
        display: flex; /* Use flexbox for alignment */
        flex-direction: column-reverse;
        justify-content: space-between; /* Space between text and image */
        align-items: center; /* Center items vertically */
    }

    .header-text {
        text-align: left; /* Align text to the left */
    }

    .header-image {
        max-width: 90vw; /* Adjust width as needed */
        height: auto; /* Maintain aspect ratio */
        margin: auto;
        border-radius: 20px;
    }
}
</style>
<header>
    <div class="header-content">
        <a href="/assets/self-portrait-close.jpg" target="_blank" class="image-link">
            <img src="/assets/self-portrait-close.jpg" alt="Joshua Zheng holding Coffee" class="header-image" />
        </a>
        <div class="header-text">
            <h1>⟨<Typing/></h1>
            <h2>
                I'm a computer science undergraduate at the University of Maryland, 
                College Park, with experience in software development, web technologies, 
                and server management. I developed the ACM website and set up a Debian server. 
                Beyond programming, I enjoy nature photography, running, and spending time with 
                my dog. Some recent projects include a web scraper for library room reservations,
                 a C compiler in Rust, and a brain-controlled hat for an RC car.     
            </h2>
        </div>
    </div>
</header>

