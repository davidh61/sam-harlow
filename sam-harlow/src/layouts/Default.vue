<template>
  <div class="layout">
    <header class="header">
      <g-link to="/contact">
        <ContactSvg :class="currentPageClass('/contact')"/>
      </g-link>

      <g-link to="/">
        <LogoSvg :class="currentPageClass('/')"/>
      </g-link>

      <g-link to="/cover-art">
        <CoverArtSvg :class="currentPageClass('/cover-art')" />
      </g-link>

      <nav class="nav"></nav>
    </header>
    <slot />
    <footer>
      <div class="socials">
        <g-link to="https://www.instagram.com/harls_98/">
          <InstagramSvg />
        </g-link>

        <g-link to="https://twitter.com/SamHarlow_">
          <TwitterSvg />
        </g-link>
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
import ContactSvg from "@/assets/images/contact.svg";
import LogoSvg from "@/assets/images/logo.svg";
import CoverArtSvg from "@/assets/images/coverart.svg";
import InstagramSvg from "@/assets/icons/instagram.svg";
import TwitterSvg from "@/assets/icons/twitter.svg";

export default {
  components: {
    ContactSvg,
    LogoSvg,
    CoverArtSvg,
    InstagramSvg,
    TwitterSvg
  },
  computed: {
    currentRouteName() {
      return this.$route.path;
    },
  },
  methods: {
    currentPageClass(path) {
      if (this.currentRouteName == path) {
        return 'current'
      }
    },
  }
};
</script>

<style lang="scss">
body {
  font-family: "Dosis", -apple-system, system-ui, BlinkMacSystemFont,
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
  padding-top: 20%;
  padding-bottom: 5%;

  svg {
    fill: #2a2a2a;
    width: 75px;
    padding-bottom: 10px;
    &:hover,
    &.current {
      fill: #2a2a2a;
      border-bottom: 5px solid #2a2a2a;
    }
  }

  .logo {
    padding-bottom: 0px;
    width: 150px;
  }
}

.socials {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
  font-size: 50px;
  justify-content: center;

  a {
    padding: 2%;
    svg {
      height: 31px;
      color: #2a2a2a;

      &:hover {
        fill: grey;
        cursor: pointer;
      }
    }
  }
}

.nav__link {
  margin-left: 20px;
}
</style>
