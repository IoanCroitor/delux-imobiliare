<script>
    import "../app.css";
    import {isUserDropdownOpen} from "$stores/OverlayStore";
    import UserDropdown from "$components/userDropdown.svelte";
    import Navigation from '$components/navigation.svelte';
    
</script>

<style>
  :global(body) {
  @apply bg-gray-900;
  }
</style>

<Navigation/>

{#if $isUserDropdownOpen}
  <UserDropdown/>
{/if}

<slot />
