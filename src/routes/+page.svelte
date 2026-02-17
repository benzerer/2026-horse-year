<script>
  import RandomImage from '../lib/RandomImage.svelte';
</script>

<main class="flex flex-col items-center justify-center min-h-screen bg-gradient-to-br from-pink-300 via-pink-200 to-orange-200 font-[Fredoka] p-8">
  <header class="text-center mb-8">
    <h1 class="text-5xl font-bold text-orange-600 drop-shadow-md">ปีนี้คุณเป็นม้าอะไร</h1>
    <p class="text-2xl text-orange-500">Discover your fortune for the year of the horse!</p>
  </header>
  <RandomImage />
</main>
