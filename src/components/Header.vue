<template>
  <div class="wrapper">
    <header>
      <div class="left__header">
        <a href="#">
          <img :src="iconLogo" alt="Logo Icon" />
        </a>
      </div>
      <div class="right__header">
        <nav>
          <ul>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Projects</a></li>
            <li><a href="#" class="contact">Contact</a></li>
          </ul>
        </nav>
      </div>

      <div class="mobile__right__header">
        <nav v-if="header" id="nav">
          <ul>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Projects</a></li>
            <li><a href="#" class="contact">Contact</a></li>
          </ul>
        </nav>

        <button class="hamburger" @click="toggleMenu">
          <img :src="iconMenu" alt="Menu" />
        </button>
      </div>
    </header>

    <main>
      <h1>{{ mainHeader }}</h1>

      <button @click="toggleArrow">
        <img :src="arrowDown" alt="Icon Arrow Down" />
      </button>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mainHeader: 'We Are Creatives',
      iconLogo: require('@/assets/images/logo.svg'),
      iconMenu: require('@/assets/images/icon-hamburger.svg'),
      arrowDown: require('@/assets/images/icon-arrow-down.svg'),
      header: false,
    };
  },

  methods: {
    toggleArrow() {
      const section = document.getElementById('section');

      window.scrollTo({
        top: section.offsetTop,
      });
    },

    toggleMenu() {
      this.header = !this.header;
    },
  },
};
</script>
