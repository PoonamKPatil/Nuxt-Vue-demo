<template>
  <div class="content">
    <AppHeader/>
    <Nuxt />
    <FooterVue/>
  </div>
</template>

<script>
import AppHeader from "~/components/AppHeader.vue"
import FooterVue from '~/components/Footer.vue'

export default {
    components: {
      AppHeader,
      FooterVue
    },
}
</script>

<style>

@import 'https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;600;700&display=swap';

body {
  background: #f2f2f2;
  color: #333;
  font-family:sans-serif;
}
a {
  color: #333;
  text-decoration: none;
}
.content {
  max-width: 960px;
  margin: 0 auto;
}
nav {
  margin: 10px auto 80px;
  padding: 10px 0;
  display: flex;
  justify-content: flex-end;
  align-items: flex-end;
  border-bottom: 1px solid #ddd;
}

nav a {
  margin-left: 12px;
}

.logo {
  margin-right: auto;
}

footer {
  display: block;
  text-align: center;
  padding: 30px 0;
  margin-top: 60px;
  color: #777;
  border-top: 1px solid #eaeaea;
}

</style>