<script>
    let name = '';
    let email = '';
    let message = '';

    function handleSubmit(event) {
        event.preventDefault();
        // Here you would handle the form submission, e.g., sending to an API
        console.log('Form submitted:', { name, email, message });
        // Reset the form
        name = '';
        email = '';
        message = '';
    }
</script>

<div class="contact-me">
    <h2>Contact Me</h2>
    <form on:submit={handleSubmit}>
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
</div>

<style>
    .contact-me {
        background: linear-gradient(to right, #E9F1F7, #FFD520);
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
