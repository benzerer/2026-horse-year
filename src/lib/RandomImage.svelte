<script>
  let imageSrc = '';

  function getRandomImage() {
    const randomIndex = Math.floor(Math.random() * 7) + 1;
    return `/images/${randomIndex}.png`;
  }

  function handleRandomize() {
    imageSrc = getRandomImage();
  }

</script>

<div class="flex flex-col items-center justify-center gap-6 p-4 w-full">
  <button on:click={handleRandomize} class="bg-orange-500 hover:bg-orange-600 text-white font-bold py-3 px-8 rounded-full transition-transform hover:scale-110">สุ่มเลยยย!!</button>
  {#if imageSrc}
    <img src={imageSrc} alt="Random result" class="max-w-full rounded-2xl shadow-lg" />
  {/if}
</div>