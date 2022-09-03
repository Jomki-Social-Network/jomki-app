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
      <div class="flex justify-between items-end row-start-1">
        <picture>
          <source srcset="jomki-banner-dark.png" media="(prefers-color-scheme: dark)">
          <img src="jomki-banner-light.png" alt="Jomki Banner">
        </picture>
        <div class="spotlight-wrapper">
          <div class="fixed -z-50 left-0 right-0 spotlight"></div>
        </div>
      </div>
      <form class="row-start-2 flex flex-col self-center bg-white shadow-md px-8 pt-6 pb-8 mb-4r gradient-border">
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="username">
            Username
          </label>
            <input class="rounded shadow appearance-none w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="username" type="text" placeholder="Username">
        </div>
        <div class="mb-6">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
            Password
          </label>
          <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" id="password" type="password" placeholder="******************">
          <p class="hidden text-red-500 text-xs italic">Please choose a password.</p>
        </div>
        <div class="flex items-center justify-between">
          <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="button">
            Sign In
          </button>
          <a class="inline-block align-baseline font-bold text-sm text-blue-500 hover:text-blue-800" href="#">
            Forgot Password?
          </a>
        </div>
      </form>
      <a href="https://github.com/Jomki-Social-Network/jomki-app" target="_blank" rel="noopener"
        class="row-start-2 cursor-pointer gradient-border col-span-3 sm:col-span-1 p-4 flex flex-col">
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
  /*position: relative;*/
  border-radius: 0.5rem;
  -webkit-backdrop-filter: blur(10px);
  backdrop-filter: blur(10px);
  /*width: 100%*/
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
  mask-composite: exclude;
  z-index: -1;
}

.gradient-border:hover::before {
  background-position: -50% 0;
  opacity: 1
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