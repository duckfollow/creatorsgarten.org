<script>
  import { onMount } from 'svelte';
  import { navigating } from '$app/stores';

  import '../app.css';
  import Navbar from '../Components/Navbar.svelte';
  import Loading from '../Components/Loading.svelte';

  onMount(() => {
    if (
      location.hostname === 'creatorsgarten.com' ||
      location.hostname === 'www.creatorsgarten.com'
    ) {
      location.replace(location.href.replace('.com', '.org'));
    }
    const flags = (new URLSearchParams(location.search).get('flags') || '').split(',');
    document.body.dataset.flags = flags.join(' ');
  });
</script>

<svelte:head>
  <title>Creatorsgarten</title>
</svelte:head>

<Navbar />

<main>
  {#if $navigating}
    <div class="h-[80vh] flex items-center justify-center">
      <Loading />
    </div>
  {:else}
    <slot />
  {/if}
</main>

<div class="cg-large-container">
  <footer class="flex justify-center py-8">© 2022 | Made with ♥ by Creatorsgarten</footer>
</div>
