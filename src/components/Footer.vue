<template>
  <footer>
    <a href="#">
      <img :src="footerLogo" alt="Footer Logo" class="footer__logo" />
    </a>

    <nav class="footer__nav">
      <ul>
        <li v-for="links in footerNav" :key="links.id">
          <a href="#">{{ links.link }}</a>
        </li>
      </ul>
    </nav>

    <div class="socials__container">
      <a href="#" v-for="images in footerSocials" :key="images.id">
        <img
          :src="images.socialIcon"
          alt="Social Icon"
          :aria-label="images.ariaLabel" />
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      footerLogo: require('@/assets/images/logo.svg'),
      footerNav: [
        {
          link: 'About',
        },
        {
          link: 'Services',
        },
        {
          link: 'Projects',
        },
      ],
      footerSocials: [
        {
          socialIcon: require('@/assets/images/icon-facebook.svg'),
          ariaLabel: 'Facebook',
        },
        {
          socialIcon: require('@/assets/images/icon-instagram.svg'),
          ariaLabel: 'Instagram',
        },
        {
          socialIcon: require('@/assets/images/icon-twitter.svg'),
          ariaLabel: 'Twitter',
        },
        {
          socialIcon: require('@/assets/images/icon-pinterest.svg'),
          ariaLabel: 'Pinterest',
        },
      ],
    };
  },
};
</script>
