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
            <div class="w-full flex-shrink-0 lg:w-3/4 lg:flex-shrink rounded-xl">
              <div class="flex space-x-4 lg:space-x-10">
                <div class="bg-gray-300 rounded-xl h-28 w-full"></div>
                <div class="bg-gray-300 rounded-xl h-28 w-full"></div>
                <div class="bg-gray-300 rounded-xl h-28 w-full"></div>
              </div>
              <div class="bg-gray-300 rounded-xl h-28 mt-4 lg:mt-10 w-full"></div>
              <div class="flex  space-x-10 mt-4 lg:mt-10">
                <div class="bg-gray-300 rounded-xl h-28 w-full"></div>
                <div class="bg-gray-300 rounded-xl h-28 w-full"></div>
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

export default {
  components: { TopNav, SidebarNav },
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
