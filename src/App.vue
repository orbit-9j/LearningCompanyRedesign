<script setup>
import { RouterLink, RouterView } from 'vue-router'
import {computed } from 'vue';
import { useRoute } from 'vue-router';

const route = useRoute();

const isHeaderVisible = computed(() => route.name !== 'feedback');
const isFooterVisible = computed(() => route.name !== 'feedback');
</script>

<template>
  <header v-if="isHeaderVisible">
    <nav>
        <div class="logo">
            <div class="logotext"><span class="pink">L</span><span class="yellow">.</span><span class="blue">C</span></div>
            <div>Learning<br>Company</div>
        </div>
        
        <!-- highlight current page -->
        <div class="buttons">
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/digitalskills">Digital Skills</RouterLink>
          <RouterLink to="/feedback">Feedback</RouterLink>
          <a class="menubutton" href="https://orbit-9j.github.io/Portfolio/" target="_blank"><button>Contact Me</button> </a>
        </div>
        </nav>
  </header>

  <RouterView />

  <footer v-if="isFooterVisible">
        <p>© 2023 by Learning Company</p>
        <div id="links">
            <a href="">Twitter</a>
            <a href="">LinkedIn</a>
        </div>
    </footer>
</template>

