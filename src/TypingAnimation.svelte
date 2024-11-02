<script>
  import { onMount } from 'svelte';

  let text = " ⟨Hi, My name is Joshua Zheng/⟩";
  let empt = " ⟨Mion g/ashZyn is J ehemH, ua⟩";
  let displayedText = "";
  let typingSpeed = 40; // Typing speed in milliseconds
  let backSpeed = 40; // Backspacing speed
  let startDelay = 1000; // Delay before starting the typing
  let backDelay = 500; // Delay after typing

  async function typeText() {
    // Start with an initial delay
    await new Promise(resolve => setTimeout(resolve, startDelay));
    
    // Typing out the full text
    for (let i = 0; i < text.length; i++) {
      displayedText = empt.slice(0, i);
      displayedText += text.slice(i, text.length);
      await new Promise(resolve => setTimeout(resolve, typingSpeed));
    }
    
    // Delay before starting the backspacing
    await new Promise(resolve => setTimeout(resolve, backDelay));

    // Backspacing with replacement by spaces
    for (let i = text.length; i > 0; i--) {
      displayedText = empt.slice(0, i);
      displayedText += text.slice(i, text.length);
      await new Promise(resolve => setTimeout(resolve, backSpeed));
    }
    
    // Restart the typing effect
    typeText();
  }

  // Start typing animation when component mounts
  onMount(() => {
    typeText();
  });
</script>

<span class="typed-me">{displayedText}</span>

<style>
  .typed-me{
    display: inline-block;    /* Allow it to respect the width */
    line-height: 1.5;        /* Adjust line-height for better readability */
    max-height: 3em;         /* Fixed height for three lines of text */
    overflow: hidden;        /* Hides overflow to avoid screen jumps */
    white-space: normal; 
  }
</style>
