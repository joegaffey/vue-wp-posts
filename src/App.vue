<template>
  <div class="wrapper">
    <div class="content">
      <img alt="Vue logo" src="./assets/logo.png" />
      <HelloWorld msg="Hello Glitch + Vue 3" />
    </div>
    <footer class="footer">
      <a className="btn--remix"
          href="https://glitch.com/edit/#!/remix/glitch-hello-react"
        >
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
  
</style>