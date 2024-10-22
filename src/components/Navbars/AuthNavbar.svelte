<script>
  import { link } from "svelte-routing";
 //import PagesDropdown from "components/Dropdowns/PagesDropdown.svelte";

  let navbarOpen = false;

  function setNavbarOpen() {
    navbarOpen = !navbarOpen;
  }
</script>

<nav class="top-0 absolute z-50 w-full flex flex-wrap items-center justify-between px-2 py-3 navbar-expand-lg">
  <div class="container px-4 mx-auto flex flex-wrap items-center justify-between">
    <div class="w-full relative flex justify-between lg:w-auto lg:static lg:block lg:justify-start">
      <a
        use:link
        class="text-white text-sm font-bold leading-relaxed inline-block mr-4 py-2 whitespace-nowrap uppercase"
        href="/"
      >
        Fabiffy
      </a>
      <button
        class="cursor-pointer text-xl leading-none  border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none h-12 w-12"
        type="button"
        on:click="{setNavbarOpen}"
      >
        <i class="text-white fas fa-bars"></i>
      </button>
    </div>
    <div
      class="lg:flex flex-grow items-center bg-white lg:bg-opacity-0 lg:shadow-none rounded shadow-lg {navbarOpen ? 'block':'hidden'}"
      id="example-navbar-warning"
    >
      <ul class="flex flex-col lg:flex-row list-none lg:ml-auto">
          <a
          use:link
          href="/"
          class="hover:text-blueGray-200 text-blueGray-100 px-3 py-2 flex items-center text-xs uppercase font-bold"
        >
        <i class="fas fa-solid fa-backward mr-2"></i> go back home </a>
      </ul>
    </div>
  </div>
</nav>
