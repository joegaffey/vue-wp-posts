<template>
  <div class="wrapper">
    <div class="content">
      <img alt="Vue logo" src="./assets/logo.png" />
      <HelloWorld msg="Hello Glitch + Vue 3" />
      
      <p class="description">
        This is a Glitch Vue starter, and it's completely customizable on Glitch!
        
        <br />
        
        This starter runs a Vue SPA (Single Page Application) using Vite without any routing. For routing, <a href="https://router.vuejs.org/">vue-router</a> is suggested.
        
        <br />
        
        While you're in the editor working, Glitch is running your start script in the background (vite dev). The site will be in dev mode and you'll see your changes happen immediately in the preview window. Once you close the editor window and your app goes to sleep, Glitch runs the build script and Vite builds your app for modern browsers.  
      </p>
    
    </div>
    <footer class="footer">
      <div class="links">
        <a href="https://vitejs.dev/guide/features.html" target="_blank">Vite Documentation</a> ·
        <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Documentation</a>
      </div>
      <a class="btn--remix" href="https://glitch.com/edit/#!/remix/glitch-hello-vue">
          <img src="https://cdn.glitch.com/a9975ea6-8949-4bab-addb-8a95021dc2da%2FLogo_Color.svg?v=1602781328576" alt="Glitch logo" />
          Remix on Glitch
      </a>
      
      
    </footer>
  </div>
</template>

<script setup>
import HelloWorld from './components/HelloWorld.vue'

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
</script>

<style>
/* Our default values set for mobile */
:root {
  --color-bg: #FFFFA0;
  --color-text-main: #2800FF;
  --color-primary: #AFECE0;
  --wrapper-height: 87vh;
  --image-max-width: 300px;
  --image-margin: 3rem;

}

/* Tablet portrait */
@media (min-width: 768px) {
  :root {
    --wrapper-height: 87vh;
    --image-max-width: 400px;
    --image-margin: 5rem;
  }
}

/* Tablet Landscape */
@media (min-width: 1024px) {
  :root {
    --wrapper-height: 87vh;
    --image-max-width: 500px;
  }
}

/* Desktop */
@media (min-width: 1280px) {
  :root {
    --wrapper-height: 87vh;
    --image-max-width: 500px;
  }
}

@font-face {
  font-family: HK Grotesk;
  src: url("https://cdn.glitch.com/a9975ea6-8949-4bab-addb-8a95021dc2da%2FHKGrotesk-Regular.otf?v=1602782380076")
    format("opentype");
}

@font-face {
  font-family: HK Grotesk;
  font-weight: bold;
  src: url("https://cdn.glitch.com/a9975ea6-8949-4bab-addb-8a95021dc2da%2FHKGrotesk-Bold.otf?v=1602782484249")
    format("opentype");
}

body {
  font-family: HK Grotesk;
  background-color: var(--color-bg);
}

.wrapper {
  min-height: var(--wrapper-height);
  display: grid;
  place-items: center;
  margin-left: 2rem;
  margin-top: 3rem;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
  
a:not(.btn--remix):link,
a:not(.btn--remix):visited {
  text-decoration: none;
  border-bottom: 6px solid var(--color-primary);
  color: var(--foreground);
  transition: background 0.2s linear;
}

a:hover {
  background: var(--color-primary);
}
  
.btn--remix {
  font-family: HK Grotesk;
  padding-left: 1rem;
  padding-right: 1rem;
  padding-top: 0.75rem;
  padding-bottom: 0.75rem;
  font-size: 1.1rem;
  line-height: 1rem;
  font-weight: 500;
  align-items: center;
  display: inline-flex;
  cursor: pointer;
  background: #FFFFFF;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 4px;
  color: #000;
  text-decoration: none;
}

.btn--remix:hover {
  background-color: #D0FFF1;
}

.btn--remix img {
  margin-right: 0.5rem;
}

.btn--remix {
  margin-right: 1rem;
}

.btn--click-me {
  user-select: none;
  cursor: pointer;
}

.btn--click-me:hover {
  text-decoration: underline;
}
  
.footer {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  padding-top: 1rem;
  width: 100%;
}

.footer a:not(.btn--remix):link,
        a:not(.btn--remix):visited {
  font-family: HK Grotesk;
  font-style: normal;
  font-weight: normal;
  font-size: 1.1rem;
  color: #000;
  text-decoration: none;
  border-style: none;
}

p {
  display: block;
  margin-top: 50px;
}
  
</style>