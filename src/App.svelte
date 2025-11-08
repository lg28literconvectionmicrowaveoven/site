<script lang="ts">
  import { Tabs } from "bits-ui";
  import {
    InstagramLogo,
    LinkedinLogo,
    GithubLogo,
    Envelope,
  } from "phosphor-svelte";
</script>

<svelte:head>
  <title>Sabarigirish Manikandan - Software Developer and Student</title>
</svelte:head>

<div
  class="flex flex-col justify-center items-center h-screen w-screen bg-gvb-bg"
>
  <div class="flex flex-col gap-6 w-full">
    <div class="max-w-4xl m-auto w-full">
      <div class="flex-1 h-2 bg-gvb-yellow mb-2"></div>
      <h1 class="m-auto text-gvb-white font-huge text-6xl pl-4 text-center">
        Sabarigirish Manikandan
      </h1>
      <p class="text-4xl text-gvb-white font-huge pl-4 m-auto text-center">
        student / developer / microwave
      </p>
      <div class="flex-1 h-2 bg-gvb-green mt-2"></div>
    </div>
    <h2 class="m-auto text-gvb-white font-sans text-xl max-w-4xl text-center">
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
      class="rounded-card border-muted shadow-card border p-3 border-gvb-white text-gvb-white m-auto w-[85%] max-w-7xl"
    >
      <Tabs.List class="ml-6 mb-4 grid grid-cols-2 gap-6">
        <Tabs.Trigger
          value="projects"
          class="data-[state=active]:text-gvb-green data-[state=active]:underline data-[state=active]:font-bold w-full m-auto border-r border-gvb-white"
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
      <Tabs.Content value="projects" class="grid grid-cols-2 w-full gap-2">
        <div
          class="border border-gvb-gray max-w-2xl m-auto size-full px-3 py-1 flex flex-col justify-center items-center"
        >
          <a
            class="font-title text-xl text-center px-1 block"
            href="https://github.com/dreamberd"
          >
            Dreamberd (WIP)
          </a>
          <div
            class="border-t border-dashed border-gvb-blue mt-1 w-full flex justify-center items-center"
          >
            <p
              class="text-gvb-white px-1.5 py-2 font-readable-sans break-normal text-center"
            >
              Developing a complete implementation of <a
                href="https://github.com/TodePond/GulfOfMexico"
                class="underline text-gvb-green hover:text-gvb-yellow italic"
              >
                Dreamberd
              </a>, the perfect programming language. Bytecode interpreter shall
              be written in Rust and VM will be written in C (I am not dealing
              with manual memory management in Rust).
            </p>
          </div>
        </div>
        <div
          class="border border-gvb-gray max-w-2xl m-auto size-full px-3 py-1 flex flex-col justify-center items-center"
        >
          <a
            class="font-title text-xl text-center px-1 block"
            href="https://github.com/rohitjg13/Campus-Crowd-Detection"
          >
            Campus Crowd Detection
          </a>
          <div
            class="border-t border-dashed border-gvb-blue mt-1 w-full flex justify-center items-center"
          >
            <p
              class="text-gvb-white px-1.5 py-2 font-readable-sans break-normal text-center"
            >
              An on-site system that accurately gauges crowd levels using audio
              cues, and Random Forest and LSTM, all done locally on a Raspberry
              Pi 5. Training data sourced from simultaneous CV using Ultralytics
              YOLO.
            </p>
          </div>
        </div>
        <div
          class="border border-gvb-gray max-w-2xl m-auto w-full px-3 py-1 col-span-2 flex flex-col justify-center items-center"
        >
          <a
            class="font-title text-xl text-center px-1 block"
            href="https://github.com/lg28literconvectionmicrowaveoven"
          >
            Open Source Contributor
          </a>
          <div
            class="border-t border-dashed border-gvb-blue mt-1 w-full flex justify-center items-center"
          >
            <div
              class="text-gvb-white px-1.5 py-2 font-readable-sans break-normal"
            >
              <ul class="list-disc ml-4">
                <li>
                  <a
                    href="https://github.com/ghostty-org/ghostty"
                    class="text-gvb-green underline italic">Ghostty</a
                  >
                </li>
                <li>
                  <a
                    href="https://github.com/johnfanv2/LenovoLegionLinux"
                    class="text-gvb-green underline italic">LenovoLegionLinux</a
                  >
                </li>
                <li>
                  <a
                    href="https://github.com/ttop32/MouseTooltipTranslator"
                    class="text-gvb-green underline italic"
                    >MouseTooltipTranslator</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
      </Tabs.Content>
      <Tabs.Content
        value="contact"
        class="w-full gap-4 flex justify-center items-center"
      >
        <a
          href="https://www.linkedin.com/in/sabarigirish-manikandan-12a90326a/"
          class="hover:text-gvb-green transition-colors"
        >
          <LinkedinLogo size={48} class="text-gvb-white hover:text-gvb-green" />
        </a>
        <a
          href="https://www.instagram.com/lg28litermicrowaveoven/"
          class="hover:text-gvb-green transition-colors"
        >
          <InstagramLogo
            size={48}
            class="text-gvb-white hover:text-gvb-green"
          />
        </a>
        <a
          href="https://github.com/lg28literconvectionmicrowaveoven"
          class="hover:text-gvb-green transition-colors"
        >
          <GithubLogo size={48} class="text-gvb-white hover:text-gvb-green" />
        </a>
        <a
          href="mailto:sabari.girish2057@gmail.com"
          class="hover:text-gvb-green transition-colors"
          ><Envelope size={48} class="text-gvb-white hover:text-gvb-green" /></a
        >
      </Tabs.Content>
    </Tabs.Root>
  </div>
</div>
