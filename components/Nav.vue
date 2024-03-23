<script setup lang='ts'>

</script>


<template>
  <nav>
    <NuxtLink to="/">Hem</NuxtLink>
    <NuxtLink to="/om-oss">Om oss</NuxtLink>
    <NuxtLink to="/vara-tjanster">Våra tjänster</NuxtLink>
    <ThemeToggle />
  </nav>
</template>


<style>
nav {
  height: 3rem;
  display: flex;
  align-items: center;
  padding: 0 1rem;
  gap: 1rem;
  justify-content: flex-start;
  border-bottom: 1px solid var(--border-color);
}

.theme-toggle {
  position: absolute;
  right: 1rem;
}
</style>