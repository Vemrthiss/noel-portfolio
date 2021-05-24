<template>
  <div class="layout">
    <header class="header">
      <div class="logo">
        <g-image src="../../static/logo.png" class="logo__image"/>
      </div>
      <nav class="nav">
        <g-link class="nav__link" to="/" exact-active-class="nav__link--active">Home</g-link>
        <g-link class="nav__link" to="/gallery" active-class="nav__link--active">Gallery</g-link>
        <g-link class="nav__link" to="/contact-me" active-class="nav__link--active">Contact Me</g-link>
      </nav>
    </header>

    <main class="main">
      <slot/>
    </main>

    <footer class="footer">
      <div class="links">
        <div class="links__left">
          <SocialmediaLink :iconObj="{iconType: 'fab', icon: 'github'}"></SocialmediaLink>
          <p class="footer__github">Created by Joel Tay</p>
        </div>

        <div class="links__right">
          <SocialmediaLink :iconObj="{iconType: 'fab', icon: 'instagram'}"></SocialmediaLink>
          <SocialmediaLink :iconObj="{iconType: 'far', icon: 'envelope'}"></SocialmediaLink>
        </div>
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
  //TO DYNAMICALLY SET TEXTFIELD SIZE BASED ON VIEWPORT WITH JS OR AT BREAKPOINTS SCALE WITH CSS?
  import SocialmediaLink from '@/components/SocialmediaLink';

  export default {
    components: {
      SocialmediaLink
    }
  }
</script>

<style lang="scss">
html {
  font-size: 62.5%;
  box-sizing: border-box;
}

*, *::before, *::after {
  box-sizing: inherit;
}

body {
  font-family: 'Montserrat', sans-serif;
  padding: 1vh 1rem;
  margin:0;
  // padding:0;
  // line-height: 1.5;
}

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: black;
  height: 13vh;
}

.logo {

  &__image {
    width: 5rem;
    height: 2rem;
  }
}

.main {
  height: 75vh;
}

.nav {

  &__link {

    &:link, &:visited {
      color: white;
    }

    &--active {
      color: red;
    }
  }
}

.footer {
  background-color: black;
  color: white;
  height: 10vh;
  position: relative;

  &__github {
    margin: 0;
    margin-left: 1rem;
    align-self: flex-end;
  }
}

.links {
  display: flex;
  justify-content: space-between;
  padding: 1rem 1.5rem;
  position: absolute;
  width: 100%;
  top: 50%;
  transform: translateY(-50%);

  &__left {
    display: flex;
  }
}

// .layout {
//   max-width: 760px;
//   margin: 0 auto;
//   padding-left: 20px;
//   padding-right: 20px;
// }

// .header {
//   display: flex;
//   justify-content: space-between;
//   align-items: center;
//   margin-bottom: 20px;
//   height: 80px;
// }

// .nav__link {
//   margin-left: 20px;
// }
</style>
