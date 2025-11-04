<script lang="ts">
  export let title: String;
  export let content: String;
</script>

<div class="m-auto w-full px-5">
  <div class="rounded-md bg-white pb-2">
    <div class="flex items-center text-black px-4 py-1 gap-2">
      <div class="rounded-xs flex-1 h-1 bg-black"></div>
      <div class="font-fancy-serif text-center whitespace-nowrap px-1">
        {title}
      </div>
      <div class="rounded-xs flex-1 h-1 bg-black"></div>
    </div>
    <div class="bg-black rounded-md mx-3">
      <p class="text-white px-2.5 py-2 font-fancy-sans">{content}</p>
    </div>
  </div>
</div>
