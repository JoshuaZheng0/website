<script>
    let name = '';
    let email = '';
    let message = '';
    let submitted = false;
    function handleSubmit() {
        submitted = true;
    }
</script>

<div class="contact-me">
    <h2>Contact Me</h2>
    {#if ! submitted}
    <form action="https://formsubmit.co/a8d6c1844f5cdd151de437268cb99911" method="POST" on:submit|preventDefault={handleSubmit}>
        <div class="form-group">
            <label for="name">Name:</label>
            <input type="text" id="name" bind:value={name} required />
        </div>
        <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" bind:value={email} required />
        </div>
        <div class="form-group">
            <label for="message">Message:</label>
            <textarea id="message" bind:value={message} rows="4" required></textarea>
        </div>
        <button type="submit">Send</button>
    </form>
    {:else}
        <p>Thank You. I will get back to you soon.</p>
    {/if}
</div>

<style>
    .contact-me {
        background: linear-gradient(to right, #ff9239, #FFD520);
        border-radius: 10px;
        padding: 20px;
        max-width: 400px; /* Adjust as needed */
        margin: auto; /* Center the form */
    }
    
    .form-group {
        margin-bottom: 15px;
    }
    
    label {
        display: block;
        margin-bottom: 5px;
        font-weight: bold;
    }
    
    input, textarea {
        width: 100%;
        padding: 10px;
        border-radius: 5px;
        border: 1px solid #ccc;
    }
    
    button {
        background-color: #008BF8;
        color: white;
        padding: 10px 15px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
        font-size: 16px;
    }
    
    button:hover {
        background-color: #007ACC;
    }
</style>
