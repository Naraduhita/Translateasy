<template>
  <div class="">
    <nav class="bg-white px-2 sm:px-4 py-2.5 dark:bg-gray-500 fixed w-full z-20 top-0 left-0 border-b border-gray-200 dark:border-gray-500">
      <div class="container flex flex-wrap items-center justify-between mx-auto">
        <!-- logo -->
        <div class="flex items-center">
          <img src="~/assets/logo.png" class="mr-4 sm:h-11" alt="Translateasy logo" />
          <span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white">Translateasyy</span>
        </div>
        <!-- profile -->
        <div class="flex md:order-2">
          <button>
            <img src="~/assets/profile.png" class="sm:h-18" alt="Profile logo" />
          </button>
        </div>
        <div class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1" id="navbar-sticky">
          <ul class="flex flex-col p-4 mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium">
            <li>
              <NuxtLink to="/" class="block py-2 pl-3 pr-4 text-white md:p-0">Translator</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about" class="block py-2 pl-3 pr-4 text-gray-400 md:p-0 md:dark:hover:text-white">About</NuxtLink>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <!-- isi -->
    <div class="bg-white rounded-2xl container mx-auto mt-64 p-2 shadow-2xl px-4">
      <div>
        <!-- <button
          id="dropdownDefaultButton"
          data-dropdown-toggle="dropdown"
          class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-4 py-2.5 mx-14 mt-8 text-center inline-flex items-center dark:bg-pink-600 dark:hover:bg-pink-400 dark:focus:ring-pink-300"
          type="button"
          v-on:click="flag ? (flag = false) : (flag = true)"
        >
          Dropdown button
          <svg class="w-4 h-4 ml-2" aria-hidden="true" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
          </svg>
        </button> -->
        <!-- Dropdown menu -->
        <!-- <div id="dropdown" class="z-10 bg-white divide-y divide-gray-100 rounded-lg shadow w-44 dark:bg-gray-700 mx-14 my-2 z-99 fixed" :class="{ hidden: flag == true }">
          <ul class="py-2 text-sm text-gray-700 dark:text-gray-200" aria-labelledby="dropdownDefaultButton">
            <li>
              <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">English</a>
            </li>
            <li>
              <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Indonesian</a>
            </li>
            <li>
              <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Japanese</a>
            </li>
            <li>
              <a href="#" class="block px-4 py-2 hover:bg-gray-100 dark:hover:bg-gray-600 dark:hover:text-white">Dutch</a>
            </li>
          </ul>
        </div> -->
        <div class="mt-6 mx-12 p-2 font-inter grid grid-cols-3 gap-1">
          <select
            id="countries"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-xl rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full px-5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500 mx-2"
          >
            <option selected>Choose a country</option>
            <option value="US">English</option>
            <option value="CA">Canada</option>
            <option value="FR">France</option>
            <option value="DE">Germany</option>
          </select>
          <!--Switch-->
          <button type="button" class="rounded-full bg-slate px-4">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-14 h-14 mx-auto rounded-full bg-slate-300 p-3 hover:bg-gray-400">
              <path stroke-linecap="round" stroke-linejoin="round" d="M7.5 21L3 16.5m0 0L7.5 12M3 16.5h13.5m0-13.5L21 7.5m0 0L16.5 12M21 7.5H7.5" />
            </svg>
          </button>
          <select
            id="countries"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-xl rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full px-5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500 -mx-2"
          >
            <option selected>Choose a country</option>
            <option value="US">English</option>
            <option value="CA">Canada</option>
            <option value="FR">France</option>
            <option value="DE">Germany</option>
          </select>
        </div>
      </div>

      <!--tabel bahasa-->
      <div class="mt-4 mx-8 mb-8 p-2 font-inter grid grid-cols-2 gap-2">
        <textarea
          cols="50"
          rows="10"
          class="mx-6 p-4 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-pink-500 focus:ring-pink-400 rounded-md sm:text-xl focus:ring-1"
          placeholder="Input text... "
        />
        <textarea
          cols="50"
          rows="10"
          class="mx-6 p-4 bg-white border shadow-sm border-slate-300 placeholder-slate-400 focus:outline-none focus:border-pink-500 focus:ring-pink-400 rounded-md sm:text-xl focus:ring-1"
          placeholder="Input text..."
        />
      </div>

      <!--Submit-->
      <div class="mt-4 mx-8 mb-8 p-2 font-inter grid grid-cols-5">
        <label></label>
        <button>
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-14 h-14 mx-40 rounded-full bg-slate-300 p-4 hover:bg-gray-200">
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M19.114 5.636a9 9 0 010 12.728M16.463 8.288a5.25 5.25 0 010 7.424M6.75 8.25l4.72-4.72a.75.75 0 011.28.53v15.88a.75.75 0 01-1.28.53l-4.72-4.72H4.51c-.88 0-1.704-.507-1.938-1.354A9.01 9.01 0 012.25 12c0-.83.112-1.633.322-2.396C2.806 8.756 3.63 8.25 4.51 8.25H6.75z"
            />
          </svg>
        </button>
        <button
          type="submit"
          class="text-white bg-pink-500 hover:bg-blue focus:ring-4 focus:outline-none focus:ring-pink-500 font-medium rounded-lg text-base w-full sm:w-auto px-5 py-2.5 text-center dark:bg-pink-500 dark:hover:bg-pink-400 dark:focus:ring-pink-500"
        >
          Submit
        </button>

        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-14 h-14 mx-14 rounded-full bg-slate-300 p-4 hover:bg-gray-200">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3 16.5v2.25A2.25 2.25 0 005.25 21h13.5A2.25 2.25 0 0021 18.75V16.5M16.5 12L12 16.5m0 0L7.5 12m4.5 4.5V3" />
        </svg>
      </div>
      <!-- <div class="py-5 px-10">
      <input
        id="text"
        class="p-5 min-w-full text-center rounded-xl bg-gray-100 rounded-3xl bg-clip-padding backdrop-filter backdrop-blur-sm bg-opacity-10 focus:outline-none text-white placeholder:text-gray-100"
        type="text"
        placeholder="type here"
      /><br />
      <div>
        <select
          name="trans"
          id="trans"
          class="px-5 mt-10 mx-auto rounded-3xl bg-gray-100 rounded-3xl bg-clip-padding backdrop-filter backdrop-blur-sm bg-opacity-10 text-white"
        >
          <option value="en">ENGLISH</option>
          <option value="id">INDO</option>
        </select>
        <div class="py-5 px-10">
          <input
            id="text"
            class="p-5 min-w-full text-center rounded-xl bg-gray-100 rounded-3xl bg-clip-padding backdrop-filter backdrop-blur-sm bg-opacity-10 focus:outline-none text-white placeholder:text-gray-100"
            type="text"
            placeholder="type here"
          /><br />
        </div>
      </div>
      <br />
      <div class="flex justify-evenly">
        <button type="submit" class="text-white font-semibold">Speak</button>
        <button type="submit" class="text-white font-semibold">
          Translate
        </button>
        <button type="submit" class="text-white font-semibold">Fusion</button>
      </div>
      <section id="translate" class="text-center pt-6 pb-2"></section>
    </div> -->
      <!-- </div> -->
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    flag: true,
  }),
};
</script>
