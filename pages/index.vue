<template>
  <body>
    <header
      class="
        fixed
        flex
        justify-between
        items-center
        px-4
        h-20
        bg-sky-900
        w-full
        md:px-12
        transition-all
        duration-500
      "
      :class="[y >= 50 ? 'h-14' : 'h-20']"
    >
      <img
        class="h-12 transition ease-out duration-500"
        :class="[y >= 50 ? 'scale-75' : 'scale-100']"
        src="https://static.vecteezy.com/system/resources/previews/002/520/838/original/apple-logo-black-isolated-on-transparent-background-free-vector.jpg"
        alt="Apple Logo"
      />

      <nav>
        <button class="md:hidden" @click="toggleNavbarState()">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6 text-white transition ease-out duration-500"
            :class="[y >= 50 ? 'scale-75' : 'scale-100']"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M4 6h16M4 12h16M4 18h16"
            />
          </svg>
        </button>

        <ul
          class="
            fixed
            w-full
            left-0
            top-20
            min-h-screen
            px-4
            pt-8
            space-y-4
            bg-sky-700
            text-white
            md:relative
            md:flex
            md:space-x-10
            md:min-h-0
            md:px-0
            md:py-0
            md:space-y-0
            md:translate-x-0
            md:top-0
          "
          :class="[navbarState ? 'translate-x-0' : 'translate-x-full']"
        >
          <li>Services</li>
          <li>Process</li>
          <li>Team</li>
          <li>Price</li>
          <li>Contact</li>
        </ul>
      </nav>
    </header>

    <section class="min-h-screen bg-green-100"></section>
  </body>
</template>

<script setup>
const navbarState = ref(false);
const toggleNavbarState = () => {
  navbarState.value = !navbarState.value;
};

const { x, y } = useWindowScroll();
</script>
