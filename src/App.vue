<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";

</script>

<template>
  <!-- <header>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Home</RouterLink>
      </nav>
    </div>
  </header> -->
  <div class="container">
    <div class="row">
      <div class="col-12 col-3-md"></div>
      <div class="col-12 col-6-md">
        <h1 class="text-center">Persona 5 Royal Confidant <br/> Schedule Search</h1>
        <p class="text-center">
          Often, persona 5 schedule guides come either in the form of long lists of dates
          or large tables. I found them cumbersome to search, so I scraped the data
          created a quick text-search version of them. Maybe you will find this useful as
          well! <br/> 
          Report issues or feature requests to <a href="https://github.com/sciku1/p5r-confidants-daily/issues">Github Repository</a>
        </p>
        <RouterView />
      </div>
      <div class="col-12 col-3-md"></div>
    </div>
  </div>
</template>

<style>
@import "https://unpkg.com/chota@latest";
:root {
  --bg-color: #ffffff;
  --bg-secondary-color: #f3f3f6;
  --color-primary: #14854f;
  --color-lightGrey: #d2d6dd;
  --color-grey: #747681;
  --color-darkGrey: #3f4144;
  --color-error: #d43939;
  --color-success: #28bd14;
  --grid-maxWidth: 120rem;
  --grid-gutter: 2rem;
  --font-size: 1.6rem;
  --font-color: #333333;
  --font-family-sans: sans-serif;
  --font-family-mono: monaco, "Consolas", "Lucida Console", monospace;
}
body.dark {
  --bg-color: #222;
  --bg-secondary-color: #444;
  --font-color: #f0f0f0;
  --color-grey: #ccc;
  --color-darkGrey: #777;
}
</style>
