<script setup lang='ts'>
useHead({
  title: 'Miniskogar',
  meta: [
    { name: 'description', content: 'En lista med tusentals växter att beställa från.' },
    { name: 'keywords', content: 'Lista, Lindersplantskola, superlista, Växter, ovanliga växter, lista att beställa ifån, 2024' },
    { name: 'author', content: 'Ugo Linder, Peter Linder' },
  ],
  bodyAttrs: {
    // class: 'test'
  },
  htmlAttrs: {
    lang: 'se',
  },
  link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com'
    },
    // {
    //   rel: 'stylesheet',
    //   href: 'https://fonts.googleapis.com/css2?family=Inter:400,500,600,700,800,900&display=swap',
    //   crossorigin: ''
    // },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Salsa&display=swap',
      crossorigin: ''
    },
    // {
    //   rel: 'stylesheet',
    //   href: 'https://fonts.googleapis.com/css2?family=Salsa:400,500,600,700,800,900&display=swap',
    //   crossorigin: ''
    // },
  ]
})
const isDark = useDark()
</script>


<template>
  <div>
    <Nav />
    <NuxtPage />
    <Footer />
  </div>
</template>


<style>
:root {
  --title-color-light: #000000;
  --title-color-dark: #fef6ec;

  --text-color-light: #4c392f;
  --text-color-dark: #eae0d4;

  --mute-text-light: #b0a99f;
  --mute-text-dark: #9a9087;

  --bg-color-light: #edebe6;
  --bg-color-dark: #181410;

  --element-bg-light: #dddad1;
  --element-bg-dark: #261f18;

  --border-color-dark: #27272a;
  --border-color-light: #ccc9c2;

  --primary-brown: #6b5e0a;
  --primary-green-dark: #8ac957;
  --primary-green-light: #76994e;
  /* --primary-green-light: #386641; */
  /* --primary-green-light: #447c4f; */
  --primary-red: #bc4749;
}

html {
  --title-color: var(--title-color-light);

  --text-color: var(--text-color-light);

  --mute-text: var(--mute-text-light);

  --bg-color: var(--bg-color-light);

  --element-bg: var(--element-bg-light);

  --border-color: var(--border-color-light);

  --primary-green: var(--primary-green-light);
}

.dark {
  --title-color: var(--title-color-dark);

  --text-color: var(--text-color-dark);

  --mute-text: var(--mute-text-dark);

  --bg-color: var(--bg-color-dark);

  --element-bg: var(--element-bg-dark);

  --border-color: var(--border-color-dark);

  --primary-green: var(--primary-green-dark);
}

html {
  min-height: 100vh;
  background: var(--bg-color);
  color: var(--text-color);
  font-family: Salsa;
}

body {
  margin: 0;
}

button,
input,
textarea {
  background: var(--element-bg);
  color: var(--text-color);
  border: none;
  padding: 0.5rem;
  border-radius: 0.5rem;
}

button {
  cursor: pointer;
}

p {
  font-size: 1.1rem;
}

h1 {
  font-size: 2.5rem;
  font-weight: 900;
  margin-bottom: 0.5rem;
}

h2 {
  font-size: 1.75rem;
  font-weight: 600
}

.page:not(.index):not(.about) {
  max-width: 60ch;
  margin: 0 auto;
}
</style>
