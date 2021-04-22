<template>
  <form action="/" method="POST">
    <div class="relative">
      <div class="w-4 text-blue-800 absolute top-3 left-3">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
          <path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd" />
        </svg>
      </div>
      <input type="text" class="w-full bg-indigo-50 rounded-md h-10 pl-10 text-indigo-900 outline-none focus:ring-4 focus:ring-blue-600">
    </div>
  </form>
</template>

<script>
export default {
  name: 'SearchForm'
}
</script>

<style scoped>

</style>
