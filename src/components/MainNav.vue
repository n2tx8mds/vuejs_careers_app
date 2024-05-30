<script setup>
  import { ref } from "vue";

  const author = ref({
    username: "n2tx8mds",
    url: "https://www.google.com",
  });
  const menuItems = ref([
    "Teams",
    "Location",
    "Life at X Corp",
    "How we hiring",
    "Students",
    "Jobs",
  ]);
</script>

<template>
  <header class="w-full text-sm">
    <div class="fixed top-0 left-0 w-full h-16 bg-white">
      <div
        class="flex flex-nowrap h-full px-8 mx-auto border-b border-solid border-gray-800"
      >
        <div class="flex flex-col justify-center">
          <a
            :href="url"
            class="flex items-center text-xl"
          >Google Careers Clone</a>
          <h2 class="text-x">
            Developed by {{ author.username }}
          </h2>
        </div>
        <nav class="h-full">
          <ul class="h-full flex items-center">
            <li>
              <a href="">Teams</a>
            </li>
            <li
              v-for="menuItem in menuItems"
              :key="menuItem"
              class="ml-9"
            >
              <a href="">{{ menuItem }}</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<style></style>
