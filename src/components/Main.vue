<template>
  <section v-for="item in content" id="section" :key="item.id">
    <div class="section__container">
      <div class="white__section">
        <h2>{{ item.headerTransform }}</h2>
        <p>{{ item.paraTransform }}</p>

        <a href="#" class="learn__more"> Learn More </a>
      </div>
      <div class="background__transform">
        <img :src="sectionEgg" alt="Egg" />
      </div>
    </div>
    <div class="section__container">
      <div class="background__standout">
        <img :src="sectionGlass" alt="Pink Cup" />
      </div>
      <div class="white__section">
        <h2>{{ item.headerStandOut }}</h2>
        <p>{{ item.paraStandOut }}</p>
        <a href="#" class="learn__more__standout"> Learn More </a>
      </div>
    </div>
  </section>
  <section
    class="section__container second__section"
    v-for="item in content"
    :key="item.id">
    <div class="graphic__container">
      <h2>{{ item.headerGraphic }}</h2>
      <p>{{ item.paraGraphic }}</p>
    </div>
    <div class="photography__container">
      <h2>{{ item.headerPhotography }}</h2>
      <p>{{ item.paraPhotography }}</p>
    </div>
  </section>

  <section class="client__container">
    <h2>{{ clientHeader }}</h2>
    <div class="client__box__container">
      <div class="client__box" v-for="items in clients" :key="items.id">
        <img :src="items.img" alt="items.name" />
        <p>{{ items.paragraph }}</p>
        <h3>{{ items.name }}</h3>
        <span>{{ items.title }}</span>
      </div>
    </div>
  </section>
  <section class="image__gallery__container">
    <div class="image__gallery__box">
      <div class="image__gallery" v-for="images in background" :key="images.id">
        <img :src="images.img" :alt="images.alt" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      clientHeader: 'Client Testimonials',
      content: [
        {
          headerTransform: 'Transform your brand',
          headerStandOut: 'Stand out to the right audience',
          headerGraphic: 'Graphic Design',
          headerPhotography: 'Photograph',
          paraTransform:
            'We are a full-servicecreative agency specializing in helping brands grow fast. Engage your clients through compelling visuals that do most of the marketing for you.',
          paraStandOut:
            'Using acollaborative formula of designers, researchers, photographers, videographers, and copywriters, we’ll build and extend your brand in digital places.',
          paraGraphic:
            'Great design makes you memorable. We deliver artwork that underscores your brand message and captures potential clients’ attention.',
          paraPhotography:
            ' Increase your credibility by getting the most stunning, high-quality photos that improve your business image.',
        },
      ],

      sectionEgg: require('@/assets/images/desktop/image-transform.jpg'),
      sectionGlass: require('@/assets/images/desktop/image-stand-out.jpg'),

      clients: [
        {
          paragraph:
            'We put our trust in Sunnyside and they delivered, making sure our needs were met and deadlines were always hit.',
          img: require('@/assets/images/image-emily.jpg'),
          name: 'Emily',
          title: 'Marketing Director',
        },
        {
          paragraph:
            'Sunnyside’s enthusiasm coupled with their keen interest in our brand’s success made it a satisfying and enjoyable experience.',
          img: require('@/assets/images/image-thomas.jpg'),
          name: 'Thomas',
          title: 'Chief Operating Office',
        },
        {
          paragraph:
            'Incredible endresult! Our sales increased over 400% when we worked with Sunnyside. Highly recommended!',
          img: require('@/assets/images/image-jennie.jpg'),
          name: 'Jennie',
          title: 'Business Owner',
        },
      ],

      background: [
        {
          img: require('@/assets/images/desktop/image-gallery-milkbottles.jpg'),
          alt: 'Milkbottles Image',
        },
        {
          img: require('@/assets/images/desktop/image-gallery-orange.jpg'),
          alt: 'Orange Image',
        },
        {
          img: require('@/assets/images/desktop/image-gallery-cone.jpg'),
          alt: 'Cone Image',
        },
        {
          img: require('@/assets/images/desktop/image-gallery-sugarcubes.jpg'),
          alt: 'Sugarcubes Image',
        },
      ],
    };
  },
};
</script>
