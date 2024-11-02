<script>
    export let title;
    export let image;
    export let description;
    export let github;
    export let imagePosition; 
    export let date;  
    export let languages;
    export let link;
</script>

<div class="project" class:image-left={imagePosition === 'left'} class:image-right={imagePosition === 'right'}>
    {#if imagePosition === 'left'}
        <img src={image} alt={title} class="project-image" />
    {/if}
    <div class="project-info" class:left-aligned={imagePosition === 'right'} class:right-aligned={imagePosition === 'left'}>
        <h3>{title} ({date})</h3>
        <p><strong>-- {languages} --</strong></p> 
        <p>{description}</p>
        <a href={github} target="_blank" rel="noopener noreferrer">Source Code</a>
        {#if link}
         | <a href={link} target="_blank" rel="noopener noreferrer">Website</a>
        {/if}
    </div>
    {#if imagePosition === 'right'}
        <img src={image} alt={title} class="project-image" />
    {/if}
</div>

<style>
    .project {
        max-height: fit-content;
        display: flex;
        align-items: flex-start; /* Align items to the top */
        justify-content: center; /* Center content horizontally */
        border-radius: 15px; /* Round corners */
        padding: .5rem; /* Adjust padding for better spacing */
        width: 100%; /* Full width of the screen */
        background: linear-gradient(135deg, #6eb2ff, #c972ff); /* Gradient background */
        margin: 20px 0; /* Space between components */
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Optional shadow for depth */
    }
    .project-image {
        max-width: 40%;
        border-radius: 10px; /* Round image corners */
        margin-right: 10px; /* Space between image and text */
    }
    .project-info {
        flex: 1; /* Allow text to take the remaining space */
    }
    .image-left .project-image {
        margin-right: 10px; /* Margin when image is on the left */
    }
    .image-right .project-image {
        margin-left: 10px; /* Margin when image is on the right */
    }
    .left-aligned {
        text-align: left; /* Align text to the left when the image is on the right */
    }
    .right-aligned {
        text-align: right; /* Align text to the right when the image is on the left */
    }
</style>
