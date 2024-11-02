<script>
    export let leadershipRoles = [];
</script>

<div class="container">
    <section class="announcements">
        <h2>Honors</h2>
        <ul>
            <li><a href="https://financialaid.umd.edu/resources-policies/presidents-scholarship-policy" class="no-style" target="_blank">UMD President’s Scholarship $12,500 yearly (2024 to 2028)</a></li>
            <li><a href="https://www.isac.org/students/before-college/college-career-planning/state-scholar-program.html" class="no-style" target="_blank">Illinois State Scholar (2024)</a></li>
            <li><a href="https://adc.d211.org/site/Default.aspx?PageID=6614" class="no-style" target="_blank">Richard C Kolze Award (2024)</a></li>
            <li><a href="https://apstudents.collegeboard.org/awards-recognitions/ap-scholar-award" class="no-style" target="_blank">AP Scholar with Distinction (2023 and 2024)</a></li>
        </ul>    
    </section>
    
    <section class="opportunities">
        <h3>Programming Languages & Frameworks</h3>
        <ul class="skills-list">
            <li><a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" class="no-style" target="_blank">JavaScript</a></li>
            <li><a href="https://www.python.org/" class="no-style" target="_blank">Python</a></li>
            <li><a href="https://reactjs.org/" class="no-style" target="_blank">React.js</a></li>
            <li><a href="https://svelte.dev/" class="no-style" target="_blank">Svelte</a></li>
            <li><a href="https://git-scm.com/" class="no-style" target="_blank">Git</a></li>
            <li><a href="https://isocpp.org/" class="no-style" target="_blank">C++</a></li>
            <li><a href="https://www.oracle.com/java/" class="no-style" target="_blank">Java</a></li>
            <li><a href="https://www.w3.org/standards/webdesign/htmlcss" class="no-style" target="_blank">HTML & CSS</a></li>
            <li><a href="https://www.mysql.com/" class="no-style" target="_blank">SQL</a></li>
            <li><a href="https://www.linux.com/" class="no-style" target="_blank">Linux Shell</a></li>
        </ul>
    
        <h3>Technologies & Tools</h3>
        <ul class="skills-list">
            <li><a href="https://pandas.pydata.org/" class="no-style" target="_blank">pandas</a></li>
            <li><a href="https://numpy.org/" class="no-style" target="_blank">Numpy</a></li>
            <li><a href="https://plotly.com/" class="no-style" target="_blank">Plotly</a></li>
            <li><a href="https://jupyter.org/" class="no-style" target="_blank">Jupyter</a></li>
            <li><a href="https://aws.amazon.com/" class="no-style" target="_blank">AWS</a></li>
            <li><a href="https://www.selenium.dev/" class="no-style" target="_blank">Selenium</a></li>
        </ul>
    </section>    
</div>

<!--
<div class="leadership">
    <h2>Leadership</h2>
    {#each leadershipRoles as role}
        <div class="leadership-item">
            <h3>{role.title}</h3>
            <p>{role.description}</p>
            {#if role.image}
                <img src={role.image} alt={role.title} class="leadership-image" />
            {/if}
        </div>
    {/each}
</div>
-->


<style>
    .leadership {
        max-width: 800px; /* Limit the width of the component */
        width: 100%; /* Full width */
        padding: 20px;
        background: linear-gradient(to right, #E9F1F7, #FFD520);
        border-radius: 10px;
        box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        margin: 0 auto; /* Center the component */
        box-sizing: border-box; /* Include padding in the element's total width */
    }
    
    .leadership-item {
        margin-bottom: 20px; /* Space between items */
        padding: 15px;
        border-radius: 5px;
        background-color: white; /* White background for contrast */
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
    }

    .leadership h3 {
        margin: 0 0 10px;
        font-size: 1.5rem;
    }

    .leadership p {
        margin: 0 0 10px;
        font-size: 1rem;
    }

    .leadership-image {
        max-width: 100%; /* Responsive image */
        height: auto; /* Maintain aspect ratio */
        border-radius: 5px;
    }
    
    .container {
        display: flex;
        justify-content: space-between;
        padding: 20px;
        gap: 20px;
    }

    .announcements, .opportunities {
        flex: 1;
        padding: 20px;
        border-radius: 10px;
        box-sizing: border-box;
    }

    .announcements {
        background: linear-gradient(
        to left, 
        #8676ff,   /* Lighter pinkish color at the top */
        #443bf7  /* Light red at the top */
        );
        color: #fff; /* Announcements text color */
    }

    .announcements h2 {
        color: #fff; 
        font-family: 'Quicksand', sans-serif; 
        font-weight: bold;
    }

    .opportunities {
        background: linear-gradient(
        to right, 
        #8676ff,   /* Lighter pinkish color at the top */
        #7329d3  /* Light red at the top */
        );
        color: #fff; /* Opportunities text color */
    }

    .announcements li {
    padding: .3vw; /* Add padding for better spacing */
    cursor: pointer; /* Change the cursor to indicate clickable items */
    transition: background-color 0.3s ease; /* Smooth transition for background color */
    }

    .announcements li:hover, .opportunities li:hover{
        background-color: rgba(255, 255, 255, 0.435); /* Lighten the background on hover */
        color: #00ff40; /* Optional: Change text color on hover */
    }

    .skills-list {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        list-style: none;
        padding: 0;
    }    
    
    .no-style {
        color: inherit; /* Inherit the text color from the parent element */
        text-decoration: none; /* Remove the underline */
    }

    .no-style:hover {
        text-decoration: underline; /* Optional: Add underline on hover */
    }

    /* Mobile Styles */
    @media only screen and (max-width: 600px) {
        .leadership {
            padding: 10px; /* Adjust padding for smaller screens */
        }

        .leadership-item {
            padding: 10px; /* Adjust item padding */
        }
        
        .leadership h3 {
            font-size: 1.2rem; /* Smaller font size for headings */
        }

        .leadership p {
            font-size: 0.9rem; /* Smaller font size for paragraphs */
        }
        .container {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            padding: 20px;
            gap: 20px;
        }

        .announcements, .opportunities {
            flex: 1;
            padding: 20px;
            border-radius: 10px;
            box-sizing: border-box;
        }

        .announcements {
            background-color: #FFEA8C; /* Announcements section color */
            color: #000000; /* Announcements text color */
        }

        .announcements h2 {
            color: #F1373A; /* Announcements heading color */
        }

        .opportunities {
            background-color: #FF787A; /* Opportunities section color */
            color: #000000; /* Opportunities text color */
        }
    }
</style>
