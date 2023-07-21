<script >
    import { fade } from "svelte/transition";
    import { isUserDropdownOpen } from "$stores/OverlayStore";
    
    const userNickname = "Ioan Croitor";
    const userEmail = "name@example.com";

    // TODO: Implement logout functionality
    function handleLogout(){
    }

    
    //Language
    //Keeps track of that is the current language
    let currentLanguage = "RO";
    let dormantLanguage = "EN";
    function languageSwitch()
    {
      let tempLanguage;
      tempLanguage = currentLanguage;
      console.log(tempLanguage);
      currentLanguage = dormantLanguage;
      console.log(currentLanguage);
      dormantLanguage = tempLanguage;
      console.log(dormantLanguage);
    }
</script>


<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="w-screen h-screen fixed top-12 right-0 z-10" on:click={() => isUserDropdownOpen.set(false)} transition:fade >
  <div class=" rounded-md relative max-w-4xl mx-auto" on:click|stopPropagation>
    <div class="flex flex-col absolute right-0 top-0 mt-2 w-60 md:w-80 rounded-xl shadow-xl bg-black/50 backdrop-blur-lg">

      <!-- Profile  -->
      <div class="p-3 flex flex-row rounded-xl bg-black/50 relative">
        <div class="w-20 h-20 md:w-32 md:h-32 rounded-full overflow-hidden group relative">
          <img class="object-cover h-full w-full group-hover:blur-lg ease-in-out duration-300" src="https://e1.pxfuel.com/desktop-wallpaper/903/679/desktop-wallpaper-97-aesthetic-best-profile-pic-for-instagram-for-boy-instagram-dp-boys.jpg" alt="Profile Icon">
          <div class="absolute inset-0 opacity-0 group-hover:opacity-100 transition duration-300 ease-in-out">
            <div class="h-full w-full bg-black/70 flex items-center justify-center">
              <a href="/settings/profile">
                <svg class="w-10 h-10 stroke-white" stroke-width="2" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M6 12h6m6 0h-6m0 0V6m0 6v6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="--darkreader-inline-stroke: #000000;" data-darkreader-inline-stroke=""></path></svg>
              </a>
            </div>
          </div>
        </div>

        <div class="ml-3 inline place-self-center">
          <p class="text-yellow-500/80">Hi, </p>
          <p class="text-xl font-bold text-gray-100">{userNickname}</p>
          <div class="text-xs rounded-full text-gray-500 hover:text-gray-300">
            {userEmail}
          </div>
        </div>
      </div>

      <!-- Dashboard -->
      <div class="pl-4 py-1.5 flex flex-row justify-start">
        <svg class="w-5 h-5 place-self-center stroke-white" stroke-width="2" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#ffffff" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M3 7.4V3.6a.6.6 0 01.6-.6h5.8a.6.6 0 01.6.6v3.8a.6.6 0 01-.6.6H3.6a.6.6 0 01-.6-.6zM14 20.4v-3.8a.6.6 0 01.6-.6h5.8a.6.6 0 01.6.6v3.8a.6.6 0 01-.6.6h-5.8a.6.6 0 01-.6-.6zM14 12.4V3.6a.6.6 0 01.6-.6h5.8a.6.6 0 01.6.6v8.8a.6.6 0 01-.6.6h-5.8a.6.6 0 01-.6-.6zM3 20.4v-8.8a.6.6 0 01.6-.6h5.8a.6.6 0 01.6.6v8.8a.6.6 0 01-.6.6H3.6a.6.6 0 01-.6-.6z" stroke-width="2" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path></svg>
        <a href="/dashboard" class="pl-1 text-md text-gray-100 hover:text-gray-200 place-self-center" >Dashboard</a>
      </div>
      <!-- New Ad -->
      <div class="pl-4 py-1.5 flex flex-row justify-start">
        <svg class="w-5 h-5 place-self-center stroke-white " stroke-width="2" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#ffffff"><path d="M8 12h4m4 0h-4m0 0V8m0 4v4M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10z" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path></svg>
        <a href="/settings" class="pl-1 text-md text-gray-100 hover:text-gray-200 place-self-center" >Post new ad</a>
      </div>
      <!-- Settings -->
      <div class="pl-4 py-1.5 flex flex-row justify-start">
        <svg class="w-5 h-5 place-self-center stroke-white" stroke-width="2" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#ffffff" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M12 15a3 3 0 100-6 3 3 0 000 6z" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path><path d="M19.622 10.395l-1.097-2.65L20 6l-2-2-1.735 1.483-2.707-1.113L12.935 2h-1.954l-.632 2.401-2.645 1.115L6 4 4 6l1.453 1.789-1.08 2.657L2 11v2l2.401.655L5.516 16.3 4 18l2 2 1.791-1.46 2.606 1.072L11 22h2l.604-2.387 2.651-1.098C16.697 18.831 18 20 18 20l2-2-1.484-1.75 1.098-2.652 2.386-.62V11l-2.378-.605z" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path></svg>
        <a href="/settings" class="pl-1 text-md text-gray-100 hover:text-gray-200 place-self-center" >Settings</a>
      </div>
      <!-- Logout -->
      <div class="pl-4 py-1.5 pb-2 flex flex-row justify-start" role="menu" aria-orientation="vertical" aria-labelledby="user-menu">
        <svg class="w-5 h-5 place-self-center stroke-red-500" stroke-width="2" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#000000"><path d="M12 12h7m0 0l-3 3m3-3l-3-3M19 6V5a2 2 0 00-2-2H7a2 2 0 00-2 2v14a2 2 0 002 2h10a2 2 0 002-2v-1" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"></path></svg>
        <a href="/" class="pl-1 text-md text-gray-100 hover:text-red-500 place-self-center" role="menuitem" on:click|preventDefault={handleLogout}>Logout</a>
      </div>
      <!-- Bottom -->
      <div class="w-full h-[1px] bg-gradient-to-r from-transparent via-white "></div>
      <div class="w-full flex flex-row justify-evenly place-self-center">
        <!-- Dark Mode -->
        <div class="h-10 flex flex-row justify-start rounded-xl">
          <svg class="w-5 h-5 place-self-center stroke-white" stroke-width="1.7" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#ffffff" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M12 18a6 6 0 100-12 6 6 0 000 12zM22 12h1M12 2V1M12 23v-1M20 20l-1-1M20 4l-1 1M4 20l1-1M4 4l1 1M1 12h1" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path></svg>
          <!-- <Switch bind:checked={}></Switch> -->
          <svg class="w-5 h-5 place-self-center stroke-white" stroke-width="1.7" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#ffffff" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M3 11.507a9.493 9.493 0 0018 4.219c-8.507 0-12.726-4.22-12.726-12.726A9.494 9.494 0 003 11.507z" stroke-width="1.7" stroke-linecap="round" stroke-linejoin="round" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path></svg>
        </div>
        <!-- Language -->
        <div class="h-10 flex flex-row justify-start rounded-xl ">
          <svg class="w-5 h-5 place-self-center stroke-white" stroke-width="1.5" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" color="#ffffff" style="--darkreader-inline-color: #e8e6e3;" data-darkreader-inline-color=""><path d="M2 12c0 5.523 4.477 10 10 10s10-4.477 10-10S17.523 2 12 2 2 6.477 2 12z" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path><path d="M13 2.05S16 6 16 12c0 6-3 9.95-3 9.95M11 21.95S8 18 8 12c0-6 3-9.95 3-9.95M2.63 15.5h18.74M2.63 8.5h18.74" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" style="--darkreader-inline-stroke: #ffffff;" data-darkreader-inline-stroke=""></path></svg>
          <p class="px-1 text-md text-gray-50 hover:text-gray-200 place-self-center" on:click={() => languageSwitch()}>{currentLanguage}</p>
          <div class="h-3 w-[1px] bg-gray-100 place-self-center"></div>
          <p class="px-1 text-md text-gray-300 hover:text-gray-200 place-self-center" on:click={() => languageSwitch()}>{dormantLanguage}</p>
        </div>
        
      </div>
    
    </div>
  </div>
</div>


