<script lang="ts">
  export let img: string = '';
  export let text: string = '';
  export let link: string = '#';
</script>

<a
  href={link}
  class="group flex flex-col bg-gray-100 border border-black relative z-10 border border-gray-900"
>
  <img
    src={img}
    alt=""
    class="object-cover brightness-[40%] group-hover:brightness-[50%] aspect-video transition-all"
  />
  <div class="flex justify-center items-center flex flex-col w-full absolute inset-0 p-4">
    <h2 class="group-hover:underline text-center text-white header">
      {text}
    </h2>
  </div>
</a>
