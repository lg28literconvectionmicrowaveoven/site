<script lang="ts">
  import { Tabs } from "bits-ui";
</script>

<svelte:head>
  <title>Sabarigirish Manikandan - Software Developer and Student</title>
</svelte:head>

<div
  class="flex flex-col justify-center items-center h-screen w-screen bg-gvb-bg"
>
  <div class="flex flex-col gap-6 w-full">
    <div class="pb-2 max-w-4xl m-auto w-full">
      <div class="flex-1 h-2 bg-gvb-yellow mb-2"></div>
      <h1 class="m-auto text-gvb-white font-huge text-6xl pl-4 text-center">
        Sabarigirish Manikandan <span class="text-4xl">
          (lg28literconvectionmicrowaveoven)
        </span>
      </h1>
      <div class="flex-1 h-2 bg-gvb-green mt-2"></div>
    </div>
    <h2
      class="m-auto text-gvb-white font-sans text-xl pl-6 pb-8 max-w-4xl text-center"
    >
      Cock emoji
    </h2>
    <Tabs.Root
      value="projects"
      class="rounded-card border-muted shadow-card border p-3 border-gvb-white text-gvb-white m-auto w-[85%] max-w-7xl"
    >
      <Tabs.List class="ml-1.5 mb-4 grid grid-cols-2 gap-6">
        <Tabs.Trigger
          value="projects"
          class="data-[state=active]:text-gvb-green data-[state=active]:underline data-[state=active]:font-bold"
        >
          Projects
        </Tabs.Trigger>
        <Tabs.Trigger
          value="contact"
          class="data-[state=active]:text-gvb-green data-[state=active]:underline data-[state=active]:font-bold"
        >
          Contact
        </Tabs.Trigger>
      </Tabs.List>
      <Tabs.Content value="projects" class="p-1">
        <div class="grid grid-cols-2 w-full">
          <div class="border border-gvb-gray pb-2 max-w-4xl m-auto w-full">
            <div class="flex items-center text-gvb-white px-4 py-1 gap-2">
              <div class="flex-1 h-1 bg-gvb-white"></div>
              <div
                class="font-title text-2xl text-center whitespace-nowrap px-1"
              >
                Dreamberd
              </div>
              <div class="flex-1 h-1 bg-gvb-white"></div>
            </div>
            <div class="border border-gvb-blue mx-3">
              <p
                class="text-gvb-white px-2.5 py-2 font-readable-sans break-normal"
              >
                Cock emoji
              </p>
            </div>
          </div>
        </div>
      </Tabs.Content>
      <Tabs.Content value="contact"></Tabs.Content>
    </Tabs.Root>
  </div>
</div>
