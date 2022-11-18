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
        <li><a href="#" @click.prevent="goSection('start')">Start</a></li>
        <li><a href="#" @click.prevent="goSection('prize')">Nagrody</a></li>
        <li>
          <a href="#" @click.prevent="goSection('instruction')"
            >Jak wziąć udział?</a
          >
        </li>
        <li>
          <a href="#" @click.prevent="goSection('examples')"
            >Przykładowe projekty</a
          >
        </li>
        <li>
          <a class="contact-btn" href="#" @click.prevent="goSection('contact')"
            >Kontakt</a
          >
        </li>
      </ul>
    </div>

    <!-- DESKTOP NAV -->
    <div class="desktop-nav">
      <nav :class="scrolled ? 'scrolled' : ''">
        <div class="logo">
          <img src="../assets/Santa_Warp.svg" alt="Warp logo" />
        </div>
        <ul>
          <li><a href="#" @click.prevent="goSection('start')">Start</a></li>
          <li><a href="#" @click.prevent="goSection('prize')">Nagrody</a></li>
          <li>
            <a href="#" @click.prevent="goSection('instruction')"
              >Jak wziąć udział?</a
            >
          </li>
          <li>
            <a href="#" @click.prevent="goSection('examples')"
              >Przykładowe projekty</a
            >
          </li>
          <li>
            <a
              class="contact-btn"
              href="#"
              @click.prevent="goSection('contact')"
              >Kontakt</a
            >
          </li>
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
      scrolled: false,
    };
  },
  methods: {
    goSection(val) {
      this.mobileNav = false;
      this.$emit('go-section', val);
    },

    handleScroll() {
      this.scrolled = window.scrollY > 0;
    },
  },
  created() {
    window.addEventListener('scroll', this.handleScroll);
  },
  destroyed() {
    window.removeEventListener('scroll', this.handleScroll);
  },
};
</script>

<style lang="scss" scoped>
@import '../styles/hamburgers.css';
@import '../styles/variables';

.mobile-navList ul li a.contact-btn,
.desktop-nav nav ul li a.contact-btn {
  color: white;
  background-color: $primary;
  border-radius: 50rem;
  padding: 1rem 2.2rem;
}
.scrolled {
  box-shadow: 0 25px 45px rgb(79 86 101 / 8%);
  transition: 0.2s ease;
}

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

  height: 30rem;
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
  .mobile-nav,
  .mobile-navList {
    display: none;
  }

  .desktop-nav {
    nav {
      position: fixed;
      z-index: 3;
      top: 0;
      left: 0;
      right: 0;
      display: flex;
      justify-content: space-between;
      align-items: center;

      height: 9rem;
      padding: 1rem 8rem;

      width: 100%;
      background-color: white;

      ul {
        display: flex;
        flex-direction: row;
        gap: 4rem;
        list-style: none;

        li {
          a {
            text-decoration: none;
            font-size: 1.6rem;
            color: $primary;
          }
        }
      }
    }
    display: flex;
    padding: 0 8rem;
    align-items: center;
    flex-direction: row;

    .logo {
      img {
        width: 6rem;
      }
    }
  }
}
</style>
