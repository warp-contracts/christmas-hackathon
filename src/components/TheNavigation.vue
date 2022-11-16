<template>
  <div>
    <!--MOBILE NAV -->
    <div class="mobile-nav">
      <nav>
        <div class="logo">
          <img src="../assets/Santa_Warp.svg" alt="Warp logo" />
        </div>
        <button
          class="hamburger hamburger--elastic"
          :class="mobileNav ? 'is-active' : ''"
          @click="mobileNav = !mobileNav"
          type="button"
        >
          <span class="hamburger-box">
            <span class="hamburger-inner"></span>
          </span>
        </button>
      </nav>
    </div>
    <div
      class="mobile-navList"
      :class="mobileNav ? 'nav-visible' : 'nav-hidden'"
    >
      <ul>
        <li><a href="#">Start</a></li>
        <li><a href="#">Jak wziąć udział?</a></li>
        <li><a href="#">Przykładowe projekty</a></li>
        <li><a href="#">Kontakt</a></li>
      </ul>
    </div>

    <!-- DESKTOP NAV -->
    <div class="desktop-nav">
      <nav>
        <div class="logo"></div>
        <ul>
          <li></li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mobileNav: false,
    };
  },
};
</script>

<style lang="scss" scoped>
@import '../styles/hamburgers.css';
@import '../styles/variables';

nav {
  position: fixed;
  z-index: 3;
  top: 0;

  width: 100%;
  background-color: white;
}

.mobile-nav > nav {
  display: flex;
  justify-content: space-between;
  align-items: center;

  height: 9rem;
  padding: 1rem 2rem;

  .logo {
    img {
      width: 6rem;
    }
  }
}

.mobile-navList {
  position: fixed;
  z-index: 2;
  top: 9rem;
  width: 100%;

  display: flex;
  justify-content: flex-end;
  align-items: center;

  height: 20rem;
  padding: 0 2rem;
  background-color: white;

  ul {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    gap: 2rem;

    width: 100%;
    list-style: none;
    border-top: 1px solid $text-basic;
    padding-top: 1rem;

    li a {
      font-size: 2rem;
      text-decoration: none;
      color: black;
      padding-top: 0.6rem;
      padding-bottom: 0.6rem;
    }
  }
}

.nav-hidden {
  transform: translateY(-105%);
  transition: 0.2s ease;
}

.nav-visible {
  transform: translateY(0);
  transition: 0.2s ease;
}
.nav-shadow {
  box-shadow: 0 25px 45px rgb(79 86 101 / 8%);
}

.desktop-nav {
  display: none;
}

@media (min-width: 768px) {
  .mobile-nav > nav {
    padding: 0 4rem;
  }
}

@media (min-width: 1023px) {
  .mobile-nav > nav {
    padding: 0 12rem;
  }
}
</style>
