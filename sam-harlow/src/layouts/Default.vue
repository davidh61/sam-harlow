<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-image src="/Images/logo.png" />
        <!-- <g-link to="/">{{ $static.metadata.siteName }}</g-link> -->
      </strong>
      <nav class="nav"></nav>
    </header>
    <slot />
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style lang="scss">
body {
  font-family: "Zilla Slab", -apple-system, system-ui, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
  background-color: white;
  color: black;
}

.layout {
  max-width: 1000px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
  font-size: 50px;
  justify-content: center;

  img {
    padding-top: 100%;
    height: 200px;
  }

}

.nav__link {
  margin-left: 20px;
}
</style>
