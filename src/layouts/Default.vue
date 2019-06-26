<template>
  <div class="container px-5 bg-background-primary text-primary md:text-xl" :class="theme">
    <header class="flex justify-between items-center mb-5 h-12 border-b border-primary">
      <strong>
        <g-link to="/">{{ $static.metaData.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
        <g-link class="nav__link" to="/about">About</g-link>
      </nav>
    </header>
    <slot/>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<script>
export default {
  data() {
    return {
      isOpen: false,
      theme: 'theme-dark',
    }
  },
}
</script>

<style src="../main.css" />

