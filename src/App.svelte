<script lang="ts">
  import { Tabs } from "bits-ui";
  import {
    InstagramLogo,
    LinkedinLogo,
    GithubLogo,
    Envelope,
  } from "phosphor-svelte";

  const LINKS = {
    instagram: "https://www.instagram.com/lg28litermicrowaveoven/",
    linkedin: "https://www.linkedin.com/in/sabarigirish-manikandan-12a90326a/",
    github: "https://github.com/lg28literconvectionmicrowaveoven",
    mail: "sabari.girish2057@gmail.com",
  };

  const DESCRIPTION = `
      I'm a student developer studying at Shiv Nadar University - Delhi NCR with
      experience in a wide variety of fields from web development to hardware
      and AI/ML. I have quickly adapted to new tech stacks on-the-fly to deliver
      on unique sets of requirements. I have experience with React.js/Next.js
      and Svelte(Kit), and built performant, scalable backends using Rust/Axum,
      GoLang, and Python/FastAPI. I have also built agentic AI systems using LangChain and LangGraph.
      I'm currently learning lower level systems programming using Rust and C.`;

  const projects = [
    {
      title: "Unlovable (WIP)",
      href: "https://github.com/lg28literconvectionmicrowaveoven/capstone-unlovable",
      description:
        "A completely local clone of lovable.dev that builds a deployment-ready NextJS application with solely text prompts and using any AI models of your choosing (including your local Ollama cluster). No coding knowledge required. Currently works off LangGraph + FastAPI local server and a Tauri app client, but a rewrite using GPUI and Rust is ongoing.",
    },
    {
      title: "Dreamberd (WIP)",
      href: "https://github.com/dreamberd",
      description: `Developing a complete implementation of <a href="https://github.com/TodePond/GulfOfMexico" class="underline text-gvb-green hover:text-gvb-yellow italic">Dreamberd</a>, "the perfect programming language". Bytecode interpreter shall be written in Rust and VM will be written in Zig.`,
    },
    {
      title: "Campus Crowd Detection",
      href: "https://github.com/rohitjg13/Campus-Crowd-Detection",
      description:
        "An on-site system that accurately gauges crowd levels using audio cues, and Random Forest and LSTM, all done locally on a Raspberry Pi 5. Training data sourced from simultaneous CV using Ultralytics YOLO.",
    },
    {
      title: "Open Source Contributor",
      href: "https://github.com/lg28literconvectionmicrowaveoven",
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

  const positions = [
    {
      title: "Development Team Member",
      organization: "SNU GDG",
      description:
        "Developed multiple projects and hosted events as a part of SNU GDG's Dev Team, namely: Campus Crowd Detection, ping v3 and v2, and FindMyDate.",
      current: true,
    },
    {
      title: "Tech Lead",
      organization: "Hackdata",
      description:
        "One of the leads in charge of SNU's premier inter-college hackathon, Hackdata. As a tech lead I'm responsible to read and approve applications and act as a liaison to the judges who are to evaluate and choose the winners.",
      current: true,
    },
    {
      title: "Tech Team Member",
      organization: "SURGE SNU",
      description:
        "Developed a dashboard page and a live-updating scoreboard for SNU's premier inter-college sporting event, SURGE.",
      current: false,
    },
    {
      title: "Web Development Intern",
      organization: "NexGen Analytix",
      description:
        "Developed a business-facing CRM with student and trainer onboarding, batch/course management, and attendance tracking and querying using Next.js, JWT-based authentication, and PostgreSQL with Prisma; with a focus on scalability and intuitive UX tailored to real-world, case-specific needs.",
      current: false,
    },
    {
      title: "Machine Learning Intern",
      organization: "DOT Glasses",
      description:
        "Conducted exploratory Data Analysis using various Machine Learning Models and interpreted data and charts to infer trends and suggest future values.",
      current: false,
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
      {DESCRIPTION}
    </h2>

    <Tabs.Root
      value="projects"
      class="rounded-card border-muted shadow-card border p-2 md:p-3 border-gvb-white text-gvb-white m-auto w-[95%] md:w-[85%] max-w-7xl"
    >
      <Tabs.List class="grid grid-cols-3 mb-3 md:mb-4 px-6 md:px-16">
        <Tabs.Trigger
          value="projects"
          class="border-r border-gvb-white px-2 md:px-8 text-center text-sm md:text-base data-[state=active]:text-gvb-green data-[state=active]:underline data-[state=active]:font-bold"
        >
          Projects
        </Tabs.Trigger>

        <Tabs.Trigger
          value="experience"
          class="border-r border-gvb-white px-2 md:px-8 text-center text-sm md:text-base data-[state=active]:text-gvb-green data-[state=active]:underline data-[state=active]:font-bold"
        >
          Experience
        </Tabs.Trigger>

        <Tabs.Trigger
          value="contact"
          class="px-2 md:px-8 text-center text-sm md:text-base data-[state=active]:text-gvb-green data-[state=active]:underline data-[state=active]:font-bold"
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
            class="border border-gvb-gray w-full h-full px-2 md:px-3 py-1 flex flex-col justify-center items-center"
          >
            <a
              class="font-title text-lg md:text-xl text-center px-1 block"
              href={project.href}
            >
              {project.title}
            </a>
            <div
              class="border-t border-dashed border-gvb-blue mt-1 w-full flex justify-center items-center grow overflow-y-auto"
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
        value="experience"
        class="grid grid-cols-1 md:grid-cols-2 w-full gap-2"
      >
        {#each positions as position}
          <div
            class="border border-gvb-gray w-full h-full px-2 md:px-3 py-1 flex flex-col justify-center items-center"
          >
            <p class="font-title text-lg md:text-xl text-center px-1 block">
              {@html `${position.title}${position.current ? " (<span class='text-gvb-aqua'>Current</span>)" : ""}`}
            </p>
            <p
              class="font-title text-lg md:text-s text-center px-1 block text-gvb-gray"
            >
              {position.organization}
            </p>
            <div
              class="border-t border-dashed border-gvb-blue mt-1 w-full flex justify-center items-center grow overflow-y-auto"
            >
              <p
                class="text-gvb-white px-1.5 py-2 font-sans break-normal text-center text-sm md:text-base"
              >
                {@html position.description}
              </p>
            </div>
          </div>
        {/each}
      </Tabs.Content>

      <Tabs.Content
        value="contact"
        class="w-full gap-3 md:gap-4 flex justify-center items-center flex-wrap"
      >
        <a href={LINKS.linkedin} class="hover:text-gvb-green transition-colors">
          <LinkedinLogo
            size={40}
            class="text-gvb-white hover:text-gvb-green md:w-12 md:h-12"
          />
        </a>
        <a
          href={LINKS.instagram}
          class="hover:text-gvb-green transition-colors"
        >
          <InstagramLogo
            size={40}
            class="text-gvb-white hover:text-gvb-green md:w-12 md:h-12"
          />
        </a>
        <a href={LINKS.github} class="hover:text-gvb-green transition-colors">
          <GithubLogo
            size={40}
            class="text-gvb-white hover:text-gvb-green md:w-12 md:h-12"
          />
        </a>
        <a
          href={`mailto:${LINKS.mail}`}
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
