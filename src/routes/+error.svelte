<script>
  import { page } from '$app/stores';
  $: title = `${$page.status}: ${String($page.error?.message)}`;
</script>

<section class="cg-container h-[80vh] flex flex-col justify-center items-center">
  <h1 class="text-2xl sm:text-4xl lg:text-5xl xl:text-6xl">¯\_(ツ)_/¯</h1>
  <h1 class="text-2xl p-2 sm:text-4xl lg:text-5xl lg:p-8 xl:text-6xl">Hmm... Nothing is here</h1>
  <p class="hidden">{title}</p>
  <a href="/" class="text-lg">Back to home</a>
</section>
