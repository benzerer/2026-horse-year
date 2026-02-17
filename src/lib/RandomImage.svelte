<script>
  import { onMount } from 'svelte';
  let imageSrc = '';

  function getRandomImage() {
    const randomIndex = Math.floor(Math.random() * 7) + 1;
    return `/images/${randomIndex}.png`;
  }

  function handleRandomize() {
    imageSrc = getRandomImage();
  }

  onMount(() => {
    imageSrc = getRandomImage();
  });
</script>

<div class="flex flex-col items-center justify-center gap-6 p-8 rounded-xl bg-white/90 shadow-lg hover:scale-105 hover:shadow-2xl transition-transform">
  <button on:click={handleRandomize} class="bg-orange-500 hover:bg-orange-600 text-white font-bold py-3 px-8 rounded-full shadow-lg transition-transform hover:scale-110">Randomize</button>
  {#if imageSrc}
    <img src={imageSrc} alt="Random result" class="max-w-xs border-8 border-orange-400 rounded-lg shadow-md" />
  {/if}
</div>