<script setup>
import { useHead } from '#imports'
const props = defineProps({
  appName: {
    type: String,
    default: "Jomki"
  },
  version: {
    type: String,
    default: ""
  },
  title: {
    type: String,
    default: "Welcome to Jomki!"
  },
  contributeOnGithub: {
    type: String,
    default: "Contribute to Jomki!"
  }
})
useHead({
  title: `${props.title}`,
  script: [],
  style: [
    {
      children: `*,:before,:after{-webkit-box-sizing:border-box;box-sizing:border-box;border-width:0;border-style:solid;border-color:#e5e7eb}*{--tw-ring-inset:var(--tw-empty, );--tw-ring-offset-width:0px;--tw-ring-offset-color:#fff;--tw-ring-color:rgba(14, 165, 233, .5);--tw-ring-offset-shadow:0 0 #0000;--tw-ring-shadow:0 0 #0000;--tw-shadow:0 0 #0000}:root{-moz-tab-size:4;-o-tab-size:4;tab-size:4}a{color:inherit;text-decoration:inherit}body{margin:0;font-family:inherit;line-height:inherit}html{-webkit-text-size-adjust:100%;font-family:ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,Segoe UI,Roboto,Helvetica Neue,Arial,Noto Sans,sans-serif,"Apple Color Emoji","Segoe UI Emoji",Segoe UI Symbol,"Noto Color Emoji";line-height:1.5}p,h4,h5{margin:0}h4,h5{font-size:inherit;font-weight:inherit}svg{display:block;vertical-align:middle}`
    }
  ]
})
</script>
<template>
  <div
    class="font-sans antialiased bg-white dark:bg-black text-black dark:text-white min-h-screen place-content-center flex flex-col items-center justify-center p-8 text-sm sm:text-base">
    <div class="grid grid-cols-3 gap-4 md:gap-8 max-w-5xl w-full z-20">
      <div class="flex justify-between items-end col-span-3">
        <picture>
          <source srcset="jomki-banner-dark.png" media="(prefers-color-scheme: dark)">
          <img src="jomki-banner-light.png" alt="Jomki Banner">
        </picture>
        <div class="spotlight-wrapper">
          <div class="fixed z-10 left-0 right-0 spotlight"></div>
        </div>
      </div>
      <div class="col-span-3 rounded p-4 flex flex-col gradient-border">
        <div class="flex justify-between items-center mb-4">
          <h4 class="font-medium text-2xl">Get Started</h4>
          <svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path
              d="M29.4284 31.095C26.9278 33.5955 23.5364 35.0003 20.0001 35.0003C16.4637 35.0003 13.0723 33.5955 10.5717 31.095C8.07118 28.5944 6.66638 25.203 6.66638 21.6667C6.66638 18.1304 8.07118 14.7389 10.5717 12.2383C10.5717 12.2383 11.6667 15 15.0001 16.6667C15.0001 13.3333 15.8334 8.33333 19.9767 5C23.3334 8.33333 26.8167 9.62833 29.4267 12.2383C30.667 13.475 31.6506 14.9446 32.321 16.5626C32.9915 18.1806 33.3355 19.9152 33.3334 21.6667C33.3357 23.418 32.9919 25.1525 32.3218 26.7705C31.6516 28.3886 30.6683 29.8582 29.4284 31.095V31.095Z"
              stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path>
            <path
              d="M16.465 26.8683C17.0456 27.4491 17.7604 27.878 18.5462 28.1169C19.3319 28.3559 20.1644 28.3976 20.9701 28.2385C21.7758 28.0793 22.5299 27.7241 23.1657 27.2043C23.8015 26.6845 24.2995 26.016 24.6157 25.2581C24.9318 24.5001 25.0564 23.6759 24.9784 22.8584C24.9004 22.0408 24.6222 21.2551 24.1684 20.5705C23.7146 19.886 23.0992 19.3238 22.3766 18.9336C21.6539 18.5434 20.8463 18.3373 20.025 18.3333L18.3333 23.3333H15C15 24.6133 15.4883 25.8933 16.465 26.8683Z"
              stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path>
          </svg>
        </div>
        <p class="mb-2">Remove this welcome page by removing <a
            class="bg-gray-100 dark:bg-white/10 rounded font-mono p-1 font-bold">&lt;NuxtWelcome /&gt;</a> tag or
          creating an <a href="https://v3.nuxtjs.org/docs/directory-structure/app" target="_blank" rel="noopener"
            class="bg-gray-100 dark:bg-white/10 rounded font-mono p-1 font-bold">app.vue</a> file.</p>
      </div>
      <a href="https://github.com/Jomki-Social-Network/jomki-app" target="_blank" rel="noopener"
        class="cursor-pointer gradient-border col-span-3 sm:col-span-1 p-4 flex flex-col">
        <svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path fill-rule="evenodd" clip-rule="evenodd"
            d="M20 3.33333C10.795 3.33333 3.33337 10.8067 3.33337 20.0283C3.33337 27.4033 8.10837 33.6617 14.7317 35.8683C15.565 36.0217 15.8684 35.5067 15.8684 35.0633C15.8684 34.6683 15.855 33.6167 15.8467 32.225C11.21 33.2333 10.2317 29.9867 10.2317 29.9867C9.47504 28.0567 8.38171 27.5433 8.38171 27.5433C6.86837 26.51 8.49671 26.53 8.49671 26.53C10.1684 26.6467 11.0484 28.25 11.0484 28.25C12.535 30.8 14.95 30.0633 15.8984 29.6367C16.0517 28.5583 16.4817 27.8233 16.9584 27.4067C13.2584 26.985 9.36671 25.5517 9.36671 19.155C9.36671 17.3333 10.0167 15.8417 11.0817 14.675C10.91 14.2533 10.3384 12.555 11.245 10.2583C11.245 10.2583 12.645 9.80833 15.8284 11.9683C17.188 11.5975 18.5908 11.4087 20 11.4067C21.4167 11.4133 22.8417 11.5983 24.1734 11.9683C27.355 9.80833 28.7517 10.2567 28.7517 10.2567C29.6617 12.555 29.0884 14.2533 28.9184 14.675C29.985 15.8417 30.6317 17.3333 30.6317 19.155C30.6317 25.5683 26.7334 26.98 23.0217 27.3933C23.62 27.9083 24.1517 28.9267 24.1517 30.485C24.1517 32.715 24.1317 34.5167 24.1317 35.0633C24.1317 35.51 24.4317 36.03 25.2784 35.8667C28.5972 34.7535 31.4823 32.6255 33.5258 29.7834C35.5694 26.9413 36.6681 23.5289 36.6667 20.0283C36.6667 10.8067 29.2034 3.33333 20 3.33333Z"
            fill="currentColor"></path>
        </svg>
        <h5 class="font-semibold text-xl mt-4">GitHub</h5>
        <p class="mt-2" v-text="contributeOnGithub" />
      </a>
    </div>
  </div>
</template>
<style scoped>

.spotlight {
  background: linear-gradient(45deg, #3256fa 0%, #C600FF 50%, #ff0000 100%);
  filter: blur(20vh);
  height: 50vh;
  bottom: -40vh
}

.spotlight-wrapper {
  opacity: 0.5;
  transition: opacity 0.4s ease-in
}

.nuxt-logo:hover~.spotlight-wrapper {
  opacity: 0.95
}

.gradient-border {
  position: relative;
  border-radius: 0.5rem;
  -webkit-backdrop-filter: blur(10px);
  backdrop-filter: blur(10px);
  width: 100%
}

@media (prefers-color-scheme: light) {
  .gradient-border {
    background-color: rgba(255, 255, 255, 0.3)
  }

  .gradient-border::before {
    background: linear-gradient(90deg, #e2e2e2 0%, #e2e2e2 25%, #3256fa 50%, #C600FF 75%, #ff0000 100%)
  }
}

@media (prefers-color-scheme: dark) {
  .gradient-border {
    background-color: rgba(20, 20, 20, 0.3)
  }

  .gradient-border::before {
    background: linear-gradient(90deg, #303030 0%, #303030 25%, #3256fa 50%, #C600FF 75%, #ff0000 100%)
  }
}

.gradient-border::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 0.5rem;
  padding: 2px;
  width: 100%;
  background-size: 400% auto;
  background-position: 0 0;
  opacity: 0.5;
  transition: background-position 0.3s ease-in-out, opacity 0.2s ease-in-out;
  -webkit-mask: linear-gradient(#fff 0 0) content-box,
    linear-gradient(#fff 0 0);
  mask: linear-gradient(#fff 0 0) content-box,
    linear-gradient(#fff 0 0);
  -webkit-mask-composite: xor;
  mask-composite: exclude
}

.gradient-border:hover::before {
  background-position: -50% 0;
  opacity: 1
}

.bg-white {
  --tw-bg-opacity: 1;
  background-color: rgba(255, 255, 255, var(--tw-bg-opacity))
}

.bg-gray-100 {
  --tw-bg-opacity: 1;
  background-color: rgba(243, 244, 246, var(--tw-bg-opacity))
}

.rounded {
  border-radius: .25rem
}

.cursor-pointer {
  cursor: pointer
}

.flex {
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex
}

.grid {
  display: -ms-grid;
  display: grid
}

.flex-col {
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -ms-flex-direction: column;
  -webkit-flex-direction: column;
  flex-direction: column
}

.place-content-center {
  place-content: center
}

.items-end {
  -webkit-box-align: end;
  -ms-flex-align: end;
  -webkit-align-items: flex-end;
  align-items: flex-end
}

.items-center {
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center
}

.justify-end {
  -webkit-box-pack: end;
  -ms-flex-pack: end;
  -webkit-justify-content: flex-end;
  justify-content: flex-end
}

.justify-center {
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center
}

.justify-between {
  -webkit-box-pack: justify;
  -ms-flex-pack: justify;
  -webkit-justify-content: space-between;
  justify-content: space-between
}

.font-sans {
  font-family: ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, Noto Sans, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", Segoe UI Symbol, "Noto Color Emoji"
}

.font-mono {
  font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, Liberation Mono, Courier New, monospace
}

.font-medium {
  font-weight: 500
}

.font-bold {
  font-weight: 700
}

.font-semibold {
  font-weight: 600
}

.text-xl {
  font-size: 1.25rem;
  line-height: 1.75rem
}

.text-sm {
  font-size: .875rem;
  line-height: 1.25rem
}

.text-2xl {
  font-size: 1.5rem;
  line-height: 2rem
}

.mb-2 {
  margin-bottom: .5rem
}

.mb-4 {
  margin-bottom: 1rem
}

.mt-4 {
  margin-top: 1rem
}

.mt-2 {
  margin-top: .5rem
}

.max-w-5xl {
  max-width: 64rem
}

.min-h-screen {
  min-height: 100vh
}

.p-4 {
  padding: 1rem
}

.p-8 {
  padding: 2rem
}

.p-1 {
  padding: .25rem
}

.pb-1 {
  padding-bottom: .25rem
}

.fixed {
  position: fixed
}

.left-0 {
  left: 0px
}

.right-0 {
  right: 0px
}

.text-black {
  --tw-text-opacity: 1;
  color: rgba(0, 0, 0, var(--tw-text-opacity))
}

.antialiased {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale
}

.w-full {
  width: 100%
}

.w-40 {
  width: 10rem
}

.z-10 {
  z-index: 10
}

.z-20 {
  z-index: 20
}

.gap-4 {
  grid-gap: 1rem;
  gap: 1rem
}

.grid-cols-3 {
  grid-template-columns: repeat(3, minmax(0, 1fr))
}

.col-span-3 {
  -ms-grid-column-span: span 3 / span 3;
  grid-column: span 3 / span 3
}

@media (min-width: 640px) {
  .sm\:text-base {
    font-size: 1rem;
    line-height: 1.5rem
  }

  .sm\:pb-2 {
    padding-bottom: .5rem
  }

  .sm\:col-span-1 {
    -ms-grid-column-span: span 1 / span 1;
    grid-column: span 1 / span 1
  }
}

@media (min-width: 768px) {
  .md\:gap-8 {
    grid-gap: 2rem;
    gap: 2rem
  }
}

@media (prefers-color-scheme: dark) {
  .dark\:bg-black {
    --tw-bg-opacity: 1;
    background-color: rgba(0, 0, 0, var(--tw-bg-opacity))
  }

  .dark\:bg-white\/10 {
    --tw-bg-opacity: .1;
    background-color: rgba(255, 255, 255, var(--tw-bg-opacity))
  }

  .dark\:text-white {
    --tw-text-opacity: 1;
    color: rgba(255, 255, 255, var(--tw-text-opacity))
  }
}
</style>