<script>

</script>

<div class="contact-me">
    <h2>Contact Me</h2>
    <form action="https://formsubmit.co/joshzcamp2018@gmail.com" method="POST" >
        <input type="hidden" name="_subject" value="New submission!"> <!-- Subject of the email -->
        <input type="hidden" name="_autoresponse" value="Thank you for your email!"> <!-- Autoresponse message -->
        <input type="hidden" name="_next" value="https://www.joshuazheng.com/"> <!-- Redirect after submission -->
        <div class="form-group">
            <label for="name">Name:</label>
            <input name="name" type="text" id="name" required />
        </div>
        <div class="form-group">
            <label for="email">Email:</label>
            <input name="email"  type="email" id="email"  required />
        </div>
        <div class="form-group">
            <label for="email">Number(optional):</label>
            <input name="number" type="tel" id="number" />
        </div>
        <div class="form-group">
            <label for="message">Message:</label>
            <textarea name="message" rows="4" required></textarea>
        </div>
        <button type="submit">Send</button>
    </form>
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
