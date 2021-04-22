<template>
  <div class="flex lg:space-x-10">
    <div class="hidden lg:w-1/2 lg:block">
      <SearchForm/>
    </div>
    <div class="w-full lg:w-1/2 border-b-2 border-indigo-600 lg:border-none">
      <div class="flex justify-between">
        <div class="lg:hidden">
          <a href="#"
             class="flex justify-center items-center w-10 h-10 rounded-xl">
            <img src="../assets/logo.jpg" class="rounded-xl" alt="">
          </a>
        </div>
        <div class="h10 hidden lg:flex items-center space-x-6 font-semibold">
          <a href="#" class="hover:text-blue-800">Feedback</a>
          <a href="#" class="hover:text-blue-800">Contracts</a>
          <a href="#" class="hover:text-blue-800">Help</a>
        </div>
        <div class="flex items-center space-x-">
          <a href="#" class="flex items-center justify-center w-10 h-10 text-gray-600 hover:text-blue-800 relative">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
              <path
                d="M10 2a6 6 0 00-6 6v3.586l-.707.707A1 1 0 004 14h12a1 1 0 00.707-1.707L16 11.586V8a6 6 0 00-6-6zM10 18a3 3 0 01-3-3h6a3 3 0 01-3 3z"/>
            </svg>
            <span class="absolute bg-red-600 h-2 w-2 top-2 right-2 rounded-full border border-white"></span>
          </a>
          <div class="lg:relative">
            <button @click="isOpen=!isOpen"
                    class="w-10 h-10 rounded-full overflow-hidden focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500 focus:ring-offset-white">
              <img
                src="https://scontent.fdac31-1.fna.fbcdn.net/v/t1.6435-9/130227399_1321934428157710_6674719724241539733_n.jpg?_nc_cat=105&ccb=1-3&_nc_sid=09cbfe&_nc_ohc=L7cYRbyJB10AX-INn3i&_nc_ht=scontent.fdac31-1.fna&oh=cee02b492574202904597f589b8990bd&oe=60A86799"
                alt="Riajul Kashem"
                class="w-10 h-10 object-cover"
              >
            </button>

            <button
              v-if="isOpen"
              @click="isOpen = false"
              class="fixed inset-0 w-full h-full z-30 cursor-default"
              tabindex="-1"
            ></button>
            <transition
              enter-active-class="transition ease-out duration-100 transform"
              enter-from-class="opacity-0 scale-95"
              enter-to-class="opacity-100 scale-100"
              leave-active-class="transition ease-in duration-75 transform"
              leave-from-class="opacity-100 scale-100"
              leave-to-class="opacity-0 scale-95"
            >
              <div v-if="isOpen"
                   class="absolute right-0 z-40 mt-2 w-full lg:w-48">
                <div class="bg-white mx-4 lg:mx-0 rounded-md shadow-lg py-1 ring-1 ring-black ring-opacity-5">
                  <div class="lg:hidden p-3">
                    <SearchForm/>
                  </div>
                  <div class="border-b-2 border-indigo-100 lg:hidden">
                    <a href="#" class="block text-left px-5 py-2 text-sm text-gray-900 hover:bg-gray-100">Feedback</a>
                    <a href="#" class="block text-left px-5 py-2 text-sm text-gray-900 hover:bg-gray-100">Contracts</a>
                    <a href="#" class="block text-left px-5 py-2 text-sm text-gray-900 hover:bg-gray-100">Help</a>
                  </div>
                  <div class="">
                    <a href="#" class="block text-left px-5 py-2 text-sm text-gray-900 hover:bg-gray-100">Profile</a>
                    <a href="#" class="block text-left px-5 py-2 text-sm text-gray-900 hover:bg-gray-100">Settings</a>
                    <a href="#" class="block text-left px-5 py-2 text-sm text-gray-900 hover:bg-gray-100">Logout</a>
                  </div>
                </div>
              </div>
            </transition>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SearchForm from './SearchForm'

export default {
  components: { SearchForm },
  name: 'TopNav',
  data () {
    return {
      isOpen: false
    }
  }
}
</script>

<style scoped>

</style>
