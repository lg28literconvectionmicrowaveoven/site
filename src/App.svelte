<script lang="ts">
  import { Tabs } from "bits-ui";
  import {
    InstagramLogo,
    LinkedinLogo,
    GithubLogo,
    Envelope,
  } from "phosphor-svelte";

  const projects = [
    {
      title: "Unlovable (WIP)",
      href: "https://github.com/capstone-unlovable",
      span: "col-span-1",
      description: `A completely local clone of unlovable that builds a deployment-ready NextJS application with solely text prompts and using any AI models of your choosing (including your local Ollama cluster). No coding knowledge required. Currently works off LangGraph and a janky Tauri app. Currently rewriting in Rust.`,
    },
    {
      title: "Dreamberd (WIP)",
      href: "https://github.com/dreamberd",
      span: "col-span-1",
      description: `Developing a complete implementation of <a href="https://github.com/TodePond/GulfOfMexico" class="underline text-gvb-green hover:text-gvb-yellow italic">Dreamberd</a>, "the perfect programming language". Bytecode interpreter shall be written in Rust and VM will be written in Zig.`,
    },
    {
      title: "Campus Crowd Detection",
      href: "https://github.com/rohitjg13/Campus-Crowd-Detection",
      span: "col-span-1",
      description: `An on-site system that accurately gauges crowd levels using audio cues, and Random Forest and LSTM, all done locally on a Raspberry Pi 5. Training data sourced from simultaneous CV using Ultralytics YOLO.`,
    },
    {
      title: "Open Source Contributor",
      href: "https://github.com/lg28literconvectionmicrowaveoven",
      span: "col-span-1",
      contributions: [
        {
          name: "FreeRDP (WIP)",
          url: "https://github.com/FreeRDP/FreeRDP/issues/7699",
          description:
            "Proper HW Decode device enumeration and selection using code from MPV.",
        },
        {
          name: "Ghostty",
          url: "https://github.com/ghostty-org/ghostty",
          description:
            "Contributed to the GPU-accelerated terminal emulator written in Zig.",
        },
        {
          name: "LenovoLegionLinux",
          url: "https://github.com/johnfanv2/LenovoLegionLinux",
          description: "Fixed dkms compilation on kernel versions >6.13.",
        },
        {
          name: "MouseTooltipTranslator",
          url: "https://github.com/ttop32/MouseTooltipTranslator",
          description: "Fixes for the real-time mouse hover translation tool.",
        },
      ],
    },
  ];
</script>

<div
  class="flex flex-col justify-center items-center min-h-screen w-screen bg-gvb-bg px-4 py-25"
>
  <div class="flex flex-col gap-4 md:gap-6 w-full">
    <div class="max-w-4xl m-auto w-full">
      <div class="flex-1 h-1.5 md:h-2 bg-gvb-yellow mb-2"></div>
      <h1
        class="m-auto text-gvb-white font-huge text-3xl sm:text-4xl md:text-5xl lg:text-6xl pl-2 md:pl-4 text-center leading-tight"
      >
        Sabarigirish Manikandan
      </h1>
      <p
        class="text-xl sm:text-2xl md:text-3xl lg:text-4xl text-gvb-white font-huge pl-2 md:pl-4 m-auto text-center mt-1"
      >
        student / developer / microwave
      </p>
      <div class="flex-1 h-1.5 md:h-2 bg-gvb-green mt-2"></div>
    </div>
    <h2
      class="m-auto text-gvb-white font-sans text-sm sm:text-base md:text-lg lg:text-xl max-w-4xl text-center px-2"
    >
      I'm a student developer studying at Shiv Nadar University - Delhi NCR with
      experience in a wide variety of fields from web development to hardware
      and AI/ML. I have quickly adapted to new tech stacks on-the-fly to deliver
      on unique sets of requirements. I have experience with React.js/Next.js
      and Svelte(Kit), and built performant, scalable backends using Rust/Axum,
      GoLang, and Python/FastAPI. I'm currently learning lower level systems
      programming using Rust and C.
    </h2>
    <Tabs.Root
      value="projects"
      class="rounded-card border-muted shadow-card border p-2 md:p-3 border-gvb-white text-gvb-white m-auto w-[95%] md:w-[85%] max-w-7xl"
    >
      <Tabs.List
        class="ml-2 md:ml-6 mb-3 md:mb-4 grid grid-cols-2 gap-3 md:gap-6"
      >
        <Tabs.Trigger
          value="projects"
          class="data-[state=active]:text-gvb-green data-[state=active]:underline data-[state=active]:font-bold w-full m-auto border-r border-gvb-white text-sm md:text-base"
        >
          Projects
        </Tabs.Trigger>
        <Tabs.Trigger
          value="contact"
          class="data-[state=active]:text-gvb-green data-[state=active]:underline data-[state=active]:font-bold text-sm md:text-base"
        >
          Contact
        </Tabs.Trigger>
      </Tabs.List>

      <Tabs.Content
        value="projects"
        class="grid grid-cols-1 md:grid-cols-2 w-full gap-2"
      >
        {#each projects as project}
          <div
            class="border border-gvb-gray w-full h-full px-2 md:px-3 py-1 flex flex-col justify-center items-center {project.span}"
          >
            <a
              class="font-title text-lg md:text-xl text-center px-1 block"
              href={project.href}
            >
              {project.title}
            </a>
            <div
              class="border-t border-dashed border-gvb-blue mt-1 w-full flex justify-center items-center flex-grow overflow-y-auto"
            >
              {#if project.contributions}
                <div class="flex flex-col gap-3 w-full py-2">
                  {#each project.contributions as item}
                    <div class="flex flex-col justify-center items-center">
                      <a
                        href={item.url}
                        class="text-gvb-green underline italic font-bold text-sm md:text-base hover:text-gvb-yellow transition-colors"
                      >
                        {item.name}
                      </a>
                      <p
                        class="text-gvb-white text-xs md:text-sm font-sans text-center px-2 opacity-90"
                      >
                        {item.description}
                      </p>
                    </div>
                  {/each}
                </div>
              {:else}
                <p
                  class="text-gvb-white px-1.5 py-2 font-sans break-normal text-center text-sm md:text-base"
                >
                  {@html project.description}
                </p>
              {/if}
            </div>
          </div>
        {/each}
      </Tabs.Content>

      <Tabs.Content
        value="contact"
        class="w-full gap-3 md:gap-4 flex justify-center items-center flex-wrap"
      >
        <a
          href="https://www.linkedin.com/in/sabarigirish-manikandan-12a90326a/"
          class="hover:text-gvb-green transition-colors"
        >
          <LinkedinLogo
            size={40}
            class="text-gvb-white hover:text-gvb-green md:w-12 md:h-12"
          />
        </a>
        <a
          href="https://www.instagram.com/lg28litermicrowaveoven/"
          class="hover:text-gvb-green transition-colors"
        >
          <InstagramLogo
            size={40}
            class="text-gvb-white hover:text-gvb-green md:w-12 md:h-12"
          />
        </a>
        <a
          href="https://github.com/lg28literconvectionmicrowaveoven"
          class="hover:text-gvb-green transition-colors"
        >
          <GithubLogo
            size={40}
            class="text-gvb-white hover:text-gvb-green md:w-12 md:h-12"
          />
        </a>
        <a
          href="mailto:sabari.girish2057@gmail.com"
          class="hover:text-gvb-green transition-colors"
          ><Envelope
            size={40}
            class="text-gvb-white hover:text-gvb-green md:w-12 md:h-12"
          /></a
        >
      </Tabs.Content>
    </Tabs.Root>
  </div>
</div>
