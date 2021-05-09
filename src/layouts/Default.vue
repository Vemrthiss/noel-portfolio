<template>
  <div class="layout">
    <div class="logo">
      <g-image src="../../static/logo.png" width="500"/>
    </div>
    <nav class="nav">
      <g-link class="nav__link" to="/" exact-active-class="nav__link--active">Home</g-link>
      <g-link class="nav__link" to="/gallery" active-class="nav__link--active">Gallery</g-link>
    </nav>

    <slot/>

    <footer class="footer">
      <div class="contact">
        <p class="contact__title">Contact Me</p>

        <form action="" class="contact__form">
          <div class="contact__name contact__form-row">
            <label for="name" class="contact__name-label contact__form-label">Name</label>
            <input name="name" type="text" class="contact__name-field contact__form-field">
          </div>
          
          <div class="contact__email contact__form-row">
            <label for="email" class="contact__email-label contact__form-label">Email</label>
            <input name="email" type="email" class="contact__email-field contact__form-field">
          </div>

          <div class="contact__message contact__form-row">
            <label for="message" class="contact__message-label contact__form-label">Message</label>
            <textarea name="message" class="contact__message-field contact__form-field" cols="30" rows="10"></textarea>
          </div>
        </form>
      </div>

      <div class="links">
        <div class="links__row">
          <svg xmlns="http://www.w3.org/2000/svg" class="links__icon icon icon-tabler icon-tabler-brand-instagram" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
            <rect x="4" y="4" width="16" height="16" rx="4" />
            <circle cx="12" cy="12" r="3" />
            <line x1="16.5" y1="7.5" x2="16.5" y2="7.501" />
          </svg>
        </div>

        <div class="links__row">
          <svg xmlns="http://www.w3.org/2000/svg" class="links__icon icon icon-tabler icon-tabler-mail" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
            <rect x="3" y="5" width="18" height="14" rx="2" />
            <polyline points="3 7 12 13 21 7" />
          </svg>
        </div>

        <div class="links__row">
          <svg xmlns="http://www.w3.org/2000/svg" class="links__icon icon icon-tabler icon-tabler-brand-github" width="44" height="44" viewBox="0 0 24 24" stroke-width="1.5" stroke="#2c3e50" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path stroke="none" d="M0 0h24v24H0z" fill="none"/>
            <path d="M9 19c-4.3 1.4 -4.3 -2.5 -6 -3m12 5v-3.5c0 -1 .1 -1.4 -.5 -2c2.8 -.3 5.5 -1.4 5.5 -6a4.6 4.6 0 0 0 -1.3 -3.2a4.2 4.2 0 0 0 -.1 -3.2s-1.1 -.3 -3.5 1.3a12.3 12.3 0 0 0 -6.2 0c-2.4 -1.6 -3.5 -1.3 -3.5 -1.3a4.2 4.2 0 0 0 -.1 3.2a4.6 4.6 0 0 0 -1.3 3.2c0 4.6 2.7 5.7 5.5 6c-.6 .6 -.6 1.2 -.5 2v3.5" />
          </svg>
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

  export default {
    
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
  // margin:0;
  // padding:0;
  // line-height: 1.5;
}

.nav {

  &__link {

    &--active {
      color: red;
    }
  }
}

.footer {
  background-color: black;
  color: white;
  display: flex;
  justify-content: space-between;
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
