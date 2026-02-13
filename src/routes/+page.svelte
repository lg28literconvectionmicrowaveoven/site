<script lang="ts">
	import { Tabs } from 'bits-ui';
	import { InstagramLogo, LinkedinLogo, GithubLogo, Envelope } from 'phosphor-svelte';

	const LINKS = {
		instagram: 'https://www.instagram.com/lg28litermicrowaveoven/',
		linkedin: 'https://www.linkedin.com/in/sabarigirish-manikandan-12a90326a/',
		github: 'https://github.com/lg28literconvectionmicrowaveoven',
		mail: 'sabari.girish2057@gmail.com'
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
			title: 'Unlovable (WIP)',
			href: 'https://github.com/lg28literconvectionmicrowaveoven/capstone-unlovable',
			description:
				'A completely local clone of lovable.dev that builds a deployment-ready NextJS application with solely text prompts and using any AI models of your choosing (including your local Ollama cluster). No coding knowledge required. Currently works off LangGraph + FastAPI local server and a Tauri app client, but a rewrite using GPUI and Rust is ongoing.'
		},
		{
			title: 'Dreamberd (WIP)',
			href: 'https://github.com/dreamberd',
			description: `Developing a complete implementation of <a href="https://github.com/TodePond/GulfOfMexico" class="underline text-gvb-green hover:text-gvb-yellow italic">Dreamberd</a>, "the perfect programming language". Bytecode interpreter shall be written in Rust and VM will be written in Zig.`
		},
		{
			title: 'Campus Crowd Detection',
			href: 'https://github.com/rohitjg13/Campus-Crowd-Detection',
			description:
				'An on-site system that accurately gauges crowd levels using audio cues, and Random Forest and LSTM, all done locally on a Raspberry Pi 5. Training data sourced from simultaneous CV using Ultralytics YOLO.'
		},
		{
			title: 'Open Source Contributor',
			href: 'https://github.com/lg28literconvectionmicrowaveoven',
			contributions: [
				{
					name: 'FreeRDP (WIP)',
					url: 'https://github.com/FreeRDP/FreeRDP/issues/7699',
					description: 'Proper HW device enumeration and selection.'
				},
				{
					name: 'Ghostty',
					url: 'https://github.com/ghostty-org/ghostty',
					description: 'Contributed to the GPU-accelerated terminal emulator written in Zig.'
				},
				{
					name: 'LenovoLegionLinux',
					url: 'https://github.com/johnfanv2/LenovoLegionLinux',
					description: 'Fixed dkms compilation on kernel versions >6.13.'
				},
				{
					name: 'MouseTooltipTranslator',
					url: 'https://github.com/ttop32/MouseTooltipTranslator',
					description: 'Fixes for the real-time mouse hover translation tool.'
				}
			]
		}
	];

	const experience = [
		{
			title: 'Development Team Member',
			organization: 'SNU GDG',
			description:
				"Developed multiple projects and hosted events as a part of SNU GDG's Dev Team, namely: Campus Crowd Detection, ping v3 and v2, and FindMyDate.",
			current: true
		},
		{
			title: 'Tech Lead',
			organization: 'Hackdata',
			description: `One of the leads in charge of SNU's premier inter-college hackathon, Hackdata. As a tech lead I'm responsible to read and approve applications and act as a liaison to the judges who are to evaluate and choose the winners. Developed <a class='underline text-gvb-green hover:text-gvb-yellow italic' href='https://hackdata.in'>ctf.hackdata.in</a> as the platform for TriNetra CTF using Python/FastAPI, Supabase, and SvelteKit. Deployed on a VPS with nginx. Developed <a class='underline text-gvb-green hover:text-gvb-yellow italic' href='https://hackdata.in'>hackdata.in</a> using SvelteKit and deployed on Vercel.`,
			current: true
		},
		{
			title: 'Paper Co-Author',
			organization: 'ISDD - 2026/BITS Pilani/MoYAS',
			description: `Co-Authored the paper <a href='/paper.pdf'>'Beyond Copyright Enforcement - Technological Protection Measures and User Rights in India'</a> which was selected to be presented at the three-day International Seminar on Digital Dreamscapes. The paper involves extensive research regarding copyright measures in software, their usages, and various cases advocating for lawful jailbreaking.`
		},
		{
			title: 'Tech Team Member',
			organization: 'SURGE SNU',
			description:
				"Developed a dashboard page and a live-updating scoreboard for SNU's premier inter-college sporting event, SURGE.",
			current: false
		},
		{
			title: 'Web Development Intern',
			organization: 'NexGen Analytix',
			description:
				'Developed a business-facing CRM with student and trainer onboarding, batch/course management, and attendance tracking and querying using Next.js, JWT-based authentication, and PostgreSQL with Prisma; with a focus on scalability and intuitive UX tailored to real-world, case-specific needs.',
			current: false
		},
		{
			title: 'Machine Learning Intern',
			organization: 'DOT Glasses',
			description:
				'Conducted exploratory Data Analysis using various Machine Learning Models and interpreted data and charts to infer trends and suggest future values.',
			current: false
		}
	];
</script>

<div class="flex min-h-screen w-screen flex-col items-center justify-center bg-gvb-bg px-4 py-25">
	<div class="flex w-full flex-col gap-4 md:gap-6">
		<div class="m-auto w-full max-w-4xl">
			<div class="mb-2 h-1.5 flex-1 bg-gvb-blue md:h-2"></div>
			<h1
				class="m-auto pl-2 text-center font-huge text-3xl leading-tight text-gvb-white sm:text-4xl md:pl-4 md:text-5xl lg:text-6xl"
			>
				Sabarigirish Manikandan
			</h1>
			<p
				class="m-auto mt-1 pl-2 text-center font-huge text-xl text-gvb-white sm:text-2xl md:pl-4 md:text-3xl lg:text-4xl"
			>
				student / developer / microwave
			</p>
			<div class="mt-2 h-1.5 flex-1 bg-gvb-green md:h-2"></div>
		</div>

		<h2
			class="m-auto max-w-4xl px-2 text-center font-sans text-sm text-gvb-white sm:text-base md:text-lg lg:text-xl"
		>
			{DESCRIPTION}
		</h2>

		<Tabs.Root
			value="projects"
			class="rounded-card border-muted shadow-card m-auto w-[95%] max-w-7xl border border-gvb-white p-2 text-gvb-white md:w-[85%] md:p-3"
		>
			<Tabs.List class="mb-3 grid grid-cols-3 px-6 md:mb-4 md:px-16">
				<Tabs.Trigger
					value="projects"
					class="border-r border-gvb-white px-2 text-center text-sm data-[state=active]:font-bold data-[state=active]:text-gvb-green data-[state=active]:underline md:px-8 md:text-base"
				>
					Projects
				</Tabs.Trigger>

				<Tabs.Trigger
					value="experience"
					class="border-r border-gvb-white px-2 text-center text-sm data-[state=active]:font-bold data-[state=active]:text-gvb-green data-[state=active]:underline md:px-8 md:text-base"
				>
					Experience
				</Tabs.Trigger>

				<Tabs.Trigger
					value="contact"
					class="px-2 text-center text-sm data-[state=active]:font-bold data-[state=active]:text-gvb-green data-[state=active]:underline md:px-8 md:text-base"
				>
					Contact
				</Tabs.Trigger>
			</Tabs.List>

			<Tabs.Content value="projects" class="grid w-full grid-cols-1 gap-2 md:grid-cols-2">
				{#each projects as project}
					<div
						class="flex h-full w-full flex-col items-center justify-center border border-gvb-gray px-2 py-1 md:px-3"
					>
						<a class="block px-1 text-center font-title text-lg md:text-xl" href={project.href}>
							{project.title}
						</a>
						<div
							class="mt-1 flex w-full grow items-center justify-center overflow-y-auto border-t border-dashed border-gvb-blue"
						>
							{#if project.contributions}
								<div class="flex w-full flex-col gap-3 py-2">
									{#each project.contributions as item}
										<div class="flex flex-col items-center justify-center">
											<a
												href={item.url}
												class="text-sm font-bold text-gvb-green italic underline transition-colors hover:text-gvb-yellow md:text-base"
											>
												{item.name}
											</a>
											<p
												class="px-2 text-center font-sans text-xs text-gvb-white opacity-90 md:text-sm"
											>
												{item.description}
											</p>
										</div>
									{/each}
								</div>
							{:else}
								<p
									class="px-1.5 py-2 text-center font-sans text-sm break-normal text-gvb-white md:text-base"
								>
									{@html project.description}
								</p>
							{/if}
						</div>
					</div>
				{/each}
			</Tabs.Content>

			<Tabs.Content value="experience" class="grid w-full grid-cols-1 gap-2 md:grid-cols-2">
				{#each experience as position}
					<div
						class="flex h-full w-full flex-col items-center justify-center border border-gvb-gray px-2 py-1 md:px-3"
					>
						<p class="block px-1 text-center font-title text-lg md:text-xl">
							{@html `${position.title}${position.current ? " (<span class='text-gvb-aqua'>Current</span>)" : ''}`}
						</p>
						<p class="md:text-s block px-1 text-center font-title text-lg text-gvb-gray">
							{position.organization}
						</p>
						<div
							class="mt-1 flex w-full grow items-center justify-center overflow-y-auto border-t border-dashed border-gvb-blue"
						>
							<p
								class="px-1.5 py-2 text-center font-sans text-sm break-normal text-gvb-white md:text-base"
							>
								{@html position.description}
							</p>
						</div>
					</div>
				{/each}
			</Tabs.Content>

			<Tabs.Content
				value="contact"
				class="flex w-full flex-wrap items-center justify-center gap-3 md:gap-4"
			>
				<a href={LINKS.linkedin} class="transition-colors hover:text-gvb-green">
					<LinkedinLogo size={40} class="text-gvb-white hover:text-gvb-green md:h-12 md:w-12" />
				</a>
				<a href={LINKS.instagram} class="transition-colors hover:text-gvb-green">
					<InstagramLogo size={40} class="text-gvb-white hover:text-gvb-green md:h-12 md:w-12" />
				</a>
				<a href={LINKS.github} class="transition-colors hover:text-gvb-green">
					<GithubLogo size={40} class="text-gvb-white hover:text-gvb-green md:h-12 md:w-12" />
				</a>
				<a href={`mailto:${LINKS.mail}`} class="transition-colors hover:text-gvb-green"
					><Envelope size={40} class="text-gvb-white hover:text-gvb-green md:h-12 md:w-12" /></a
				>
			</Tabs.Content>
		</Tabs.Root>
	</div>
</div>
