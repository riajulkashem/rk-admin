<template>
  <div class="flex h-full">
    <div class="fixed lg:static lg:w-24 bottom-0 w-full lg:h-full z-10">
      <div class="w-full lg:w-24 h-full bg-blue-800 relative">
        <a href="#"
          class="hidden absolute top-10 left-1/2 transform -translate-x-1/2 lg:block w-14 h-14 bg-white rounded-xl">
          <img src="./assets/logo.jpg" class="rounded-xl" alt="">
        </a>
        <SidebarNav />
      </div>
    </div>
    <div class="w-full lg:p-10 p-4">
      <TopNav />
      <div class="bg-gray-300 rounded-xl lg:hidden mt-4 p-2">
        <button class="block w-32 h-10 bg-blue-600 mx-auto" @click="showSideBar = !showSideBar">Toggle Side Bar</button>
      </div>
      <div class="overflow-hidden">
        <div class="transform lg:transform-none transition-all duration-300" :class="showSideBar ? '-translate-x-full': ''">
          <div class="flex lg:mt-10 mt-4 space-x-0 lg:space-x-10">
            <div class="w-full flex-shrink-0 lg:w-3/4 lg:flex-shrink rounded-xl mb-60 lg:mb-0">
              <div class="flex space-x-4 lg:space-x-10">
                <div class="widget-card">
                  <div class="widget-card-icon">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                      <path d="M2 11a1 1 0 011-1h2a1 1 0 011 1v5a1 1 0 01-1 1H3a1 1 0 01-1-1v-5zM8 7a1 1 0 011-1h2a1 1 0 011 1v9a1 1 0 01-1 1H9a1 1 0 01-1-1V7zM14 4a1 1 0 011-1h2a1 1 0 011 1v12a1 1 0 01-1 1h-2a1 1 0 01-1-1V4z" />
                    </svg>
                  </div>
                  <div class="w-1/3 bg-white">
                    <div class="widget-card-title">Visitors</div>
                    <div class="widget-card-value">3,255</div>
                  </div>
                </div>

                <div class="widget-card">
                  <div class="widget-card-icon">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                      <path d="M2 11a1 1 0 011-1h2a1 1 0 011 1v5a1 1 0 01-1 1H3a1 1 0 01-1-1v-5zM8 7a1 1 0 011-1h2a1 1 0 011 1v9a1 1 0 01-1 1H9a1 1 0 01-1-1V7zM14 4a1 1 0 011-1h2a1 1 0 011 1v12a1 1 0 01-1 1h-2a1 1 0 01-1-1V4z" />
                    </svg>
                  </div>
                  <div class="w-1/3 bg-white">
                    <div class="widget-card-title">Visitors</div>
                    <div class="widget-card-value">3,255</div>
                  </div>
                </div>

                <div class="widget-card-active">
                  <div class="widget-card-icon-active">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                      <path d="M2 11a1 1 0 011-1h2a1 1 0 011 1v5a1 1 0 01-1 1H3a1 1 0 01-1-1v-5zM8 7a1 1 0 011-1h2a1 1 0 011 1v9a1 1 0 01-1 1H9a1 1 0 01-1-1V7zM14 4a1 1 0 011-1h2a1 1 0 011 1v12a1 1 0 01-1 1h-2a1 1 0 01-1-1V4z" />
                    </svg>
                  </div>
                  <div class="w-1/3 bg-red-500">
                    <div class="widget-card-title widget-card-text-color">Visitors</div>
                    <div class="widget-card-value widget-card-text-color">3,255</div>
                  </div>
                </div>
              </div>
              <div class="flex  space-x-10 mt-4 lg:mt-10">
                <Blog />
              </div>
            </div>
            <div class="w-full lg:w-1/4 flex-shrink-0 lg:flex-shrink bg-gray-300 rounded-xl h-52">Sidebar</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script type='text/javascript'>
import SidebarNav from './components/SidebarNav'
import TopNav from './components/TopNav'
import Blog from './components/Blog'

export default {
  components: { TopNav, SidebarNav, Blog },
  data () {
    return {
      showSideBar: false
    }
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
