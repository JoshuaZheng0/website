<script>
    import { onMount } from 'svelte';
  
    let text = " Hi, My name is Joshua Zheng/⟩";
    let displayedText = "";
    let typingSpeed = 40; // Typing speed in milliseconds
    let backSpeed = 40; // Backspacing speed
    let startDelay = 1000; // Delay before starting the typing
    let backDelay = 500; // Delay after backspacing
  
    async function typeText() {
      await new Promise(resolve => setTimeout(resolve, startDelay));
      for (let i = 0; i < text.length; i++) {
        displayedText += text[i];
        await new Promise(resolve => setTimeout(resolve, typingSpeed));
      }
      await new Promise(resolve => setTimeout(resolve, backDelay));
      for (let i = text.length; i > 0; i--) {
        displayedText = displayedText.slice(0, i);
        await new Promise(resolve => setTimeout(resolve, backSpeed));
      }
      typeText(); // Repeat the typing effect
    }
  
    // Start typing animation when component mounts
    onMount(() => {
      typeText();
    });
  </script>
  
  <span class="typed-me">{displayedText}</span>
  