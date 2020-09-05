<template>
  <header class="border-t-14 border-teal-300">
    <nav class="container mx-auto flex flex-wrap justify-between items-center py-8">
      <div>
        <g-link v-if="theme === 'theme-light'" to="/">
          <g-image src="../../../static/img/logo.png" class="w-32" alt="logo"/>
        </g-link>
        <g-link v-else to="/">
          <g-image src="../../../static/img/logo.png" class="w-32" alt="logo"/>
        </g-link>
      </div>
      <div class="block lg:hidden">
        <button @click="toggle"
                class="flex items-center px-3 py-2 border rounded border-gray-500 hover:text-gray-600 hover:border-gray-600"
                data-cypress="hamburger">
          <svg class="current-color h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
            <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" fill="gray"/>
          </svg>
        </button>
      </div>
      <ul
          class="uppercase tracking-wide font-bold w-full block flex-grow lg:space-x-8 space-y-6 lg:space-y-0 lg:flex lg:flex-initial lg:w-auto items-center mt-8 lg:mt-0"
          :class="isOpen ? 'block': 'hidden'"
          data-cypress="menu"
      >
        <!--          <li class="mb-6 lg:mb-0">-->
        <!--            <search-input />-->
        <!--          </li>-->
        <li>
          <theme-switcher :theme="theme" @themeChanged="updateTheme"/>
        </li>
        <li>
          <a v-if="$route.path === '/'" href="/#projects" v-scroll-to="'#projects'"
             class="text-copy-primary hover:text-gray-600" data-cypress="projects">HOME</a>
          <g-link v-else to="/#projects" class="text-copy-primary hover:text-gray-600">HOME</g-link>
        </li>
        <li>
          <a v-if="$route.path === '/'" href="/#about" v-scroll-to="'#about'"
             class="text-copy-primary hover:text-gray-600" data-cypress="about">ABOUT US</a>
          <g-link v-else to="/#about" class="text-copy-primary hover:text-gray-600">ABOUT US</g-link>
        </li>
        <li>
          <a v-if="$route.path === '/'" href="/#contact" v-scroll-to="'#contact'"
             class="text-copy-primary hover:text-gray-600" data-cypress="contact">FEATURED WORKS</a>
          <g-link v-else to="/#contact" class="text-copy-primary hover:text-gray-600">FEATURED WORKS</g-link>
        </li>
        <li>
          <a v-if="$route.path === '/'" href="/#contact" v-scroll-to="'#contact'"
             class="text-copy-primary hover:text-gray-600" data-cypress="contact">OUR SERVICES</a>
          <g-link v-else to="/#contact" class="text-copy-primary hover:text-gray-600">OUR SERVICES</g-link>
        </li>
        <li>
          <a v-if="$route.path === '/'" href="/#contact" v-scroll-to="'#contact'"
             class="text-copy-primary hover:text-gray-600" data-cypress="contact">SMALL TEAM</a>
          <g-link v-else to="/#contact" class="text-copy-primary hover:text-gray-600">SMALL TEAM</g-link>
        </li>
        <!--          <li>-->
        <!--            <a v-if="$route.path === '/'" href="/#contact" v-scroll-to="'#contact'" class="text-copy-primary hover:text-gray-600" data-cypress="contact">WHAT THEY SAYS</a>-->
        <!--            <g-link v-else to="/#contact" class="text-copy-primary hover:text-gray-600">WHAT THEY SAYS</g-link>-->
        <!--          </li>-->
        <!--          <li>-->
        <!--            <a v-if="$route.path === '/'" href="/#contact" v-scroll-to="'#contact'" class="text-copy-primary hover:text-gray-600" data-cypress="contact">LOGOCEM</a>-->
        <!--            <g-link v-else to="/#contact" class="text-copy-primary hover:text-gray-600">LOGOCEM</g-link>-->
        <!--          </li>-->
        <li>
          <a v-if="$route.path === '/'" href="/#contact" v-scroll-to="'#contact'"
             class="text-copy-primary hover:text-gray-600" data-cypress="contact">CONTACT</a>
          <g-link v-else to="/#contact" class="text-copy-primary hover:text-gray-600">CONTACT</g-link>
        </li>
        <!--          <li>-->
        <!--            <g-link to="/docs" class="text-copy-primary hover:text-gray-600" data-cypress="docs">Docs</g-link>-->
        <!--          </li>-->
        <!--          <li>-->
        <!--            <g-link to="/blog" class="text-copy-primary hover:text-gray-600" data-cypress="blog">Blog</g-link>-->
        <!--          </li>-->
      </ul>
    </nav>
  </header>
</template>

<script>
import ThemeSwitcher from "../ThemeSwitcher";

export default {
  name: "Header",
  components: {ThemeSwitcher},
  mounted() {
    this.theme = localStorage.getItem('theme') || 'theme-light'
  },
  data() {
    return {
      isOpen: false,
      theme: '',
    }
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen
    },
    updateTheme(theme) {
      this.theme = theme
    }
  }
}
</script>

<style scoped>

</style>