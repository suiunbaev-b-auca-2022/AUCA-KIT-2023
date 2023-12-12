<!-- src/routes/_layout.svelte
<script>
    import { onMount } from 'svelte';
  
    let isBurgerOpen = false;
  
    onMount(() => {
      const burgerToggle = document.getElementById('burger-toggle');
      burgerToggle.addEventListener('change', () => {
        isBurgerOpen = burgerToggle.checked;
      });
    });
  </script>
  
  <header class="menu">
    <a href="/home" class="logo">
      <img
        src="https://media.licdn.com/dms/image/C4D0BAQEe7Oqy-M7jBQ/company-logo_200_200/0/1638280750854?e=2147483647&v=beta&t=rgqHo1h-U3sMtsFXuRW74FDYbfLkPOikbcKBnM5GkHc"
        alt="Company Logo"
        class="logo-image"
      />
    </a>
  
    <input type="checkbox" id="burger-toggle" />
    <label for="burger-toggle" class="burger">
      <div class="line"></div>
      <div class="line"></div>
      <div class="line"></div>
    </label>
  
    <label for="burger-toggle" class="cross">
      <p>X</p>
    </label>
  
    <nav class="menu1" bind:class="{ 'menu1-open': isBurgerOpen }">
      <ul class="menu-items">
        <li><a href="/home">Home</a></li>
        <li><a href="/about">About</a></li>
        <li><a href="/services">Services</a></li>
        <li><a href="/contact">Contact</a></li>
        <li><a href="https://github.com/suiunbaev-b-auca-2022/githubpages2/blob/main/goals.md">Info</a></li>
      </ul>
    </nav>
  </header>
  
  <main>
    <slot></slot>
  </main>
  
  <footer>&copy; 2023 My Website</footer>
  
  <style>
    /* Add your existing styles here */
  
    .menu1-open {
      display: block;
      right: 0px;
    }
  </style>
   -->
