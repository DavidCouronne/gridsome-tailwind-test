<template>
  <div class="layout bg-background-primary" :class="theme">
    <header class="header">
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
      theme: 'theme-light',
    }
  },
}
</script>

<style src="../main.css" />

