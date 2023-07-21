<script>
    
    import {isUserDropdownOpen} from "$stores/OverlayStore.js"
    
    function handleLogout() {
      // TODO: Implement logout functionality
    }

    let unreadMessageCount=0;
</script>


<nav class="sticky top-0 nav px-3 dark:bg-black/90 bg-white/90 backdrop-blur b-2 z-10">
  <div class="flex flex-wrap items-center justify-between max-w-7xl mx-auto">
  
    <a href="/">
        <div class="w-10 h-10 m-2">
            <img class="hidden dark:block user-select-none pointer-events-none" src="../../src/Images/delux_b&w_navbar_white.png" alt="Delux logo" >
            <img class="dark:hidden user-select-none pointer-events-none" src="../../src/Images/delux_b&w_navbar_dark.png" alt="Delux logo" >
        </div>
    </a>


    <div class="flex flex-row h-12 items-center">

        <a href="/favourites/" class="pr-2">
          <div >
            <svg class="w-6 h-6 stroke-red-500 hover:stroke-red-500 hover:fill-red-500" stroke-width="2" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#ffffff" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M22 8.862a5.95 5.95 0 01-1.654 4.13c-2.441 2.531-4.809 5.17-7.34 7.608-.581.55-1.502.53-2.057-.045l-7.295-7.562c-2.205-2.286-2.205-5.976 0-8.261a5.58 5.58 0 018.08 0l.266.274.265-.274A5.612 5.612 0 0116.305 3c1.52 0 2.973.624 4.04 1.732A5.95 5.95 0 0122 8.862z" stroke-width="2" stroke-linejoin="round" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path></svg>
          </div>
        </a>

        <a href="/messages/" class="pr-2">
          {#if unreadMessageCount > 0}
          <div class="relative group">
            <svg class="w-6 h-6 stroke-white group-hover:stroke-gray-200 transition ease-in-out duration-150" stroke-width="2" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M7 12h10M7 8h6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path><path d="M3 20.29V5a2 2 0 012-2h14a2 2 0 012 2v10a2 2 0 01-2 2H7.961a2 2 0 00-1.561.75l-2.331 2.914A.6.6 0 013 20.29z" stroke-width="2" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path></svg>
            <div class="absolute bottom-0 right-0 w-3 h-3 rounded-full flex items-center justify-center  text-white overflow-hidden bg-fuchsia-700 group-hover:scale-125 transition ease-in-out duration-150">
              <p class="text-[8px] font-bold text-white">15</p>
            </div>
          </div>
          {:else}
            <svg class="w-6 h-6 stroke-white hover:stroke-gray-200 transition ease-in-out duration-150  " stroke-width="2" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#ffffff" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M3 20.29V5a2 2 0 012-2h14a2 2 0 012 2v10a2 2 0 01-2 2H7.961a2 2 0 00-1.561.75l-2.331 2.914A.6.6 0 013 20.29z" stroke-width="2" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path></svg>
          {/if}
        </a>


        <div class="relative z-auto">
          <button class="inline-block" on:click={() => isUserDropdownOpen.set(true)}>
            <img class="w-10 h-10 rounded-full overflow-hidden user-select-none pointer-events-none" src="../../src/Images/user.jpg" alt="User Icon">
          </button>
        </div>
    </div>
  </div>
</nav>

