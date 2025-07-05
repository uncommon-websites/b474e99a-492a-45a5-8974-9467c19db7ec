<script lang="ts">
	// Types

	// Components
	import SectionHeader from "$lib/components/layout/SectionHeader.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Card from "$lib/components/ui/Card.svelte";
	import JobList, { type JobOpening } from "./JobList.svelte";

	// Icons
	import IconBriefcase from "$lib/components/icons/Briefcase.svelte";
	import IconUsers from "$lib/components/icons/Users.svelte";
	import IconHeart from "$lib/components/icons/Heart.svelte";
	import IconGlobe from "$lib/components/icons/Globe.svelte";

	// Constants
	const SECTION_BASE_CLASSES = "section-py section-px container mx-auto";
	const GRADIENT_BG_CLASSES =
		"bg-gradient-to-br from-gray-50 to-gray-100 dark:from-gray-900 dark:to-gray-800";
	const ICON_CONTAINER_CLASSES =
		"bg-primary-50 text-primary-600 dark:bg-primary-950 dark:text-primary-400 flex items-center justify-center rounded-full";

	const benefits = [
		{
			title: "Cutting-edge AI research",
			description: "Work at the forefront of artificial intelligence, developing solutions that advance scientific discovery.",
			icon: IconBriefcase
		},
		{
			title: "Impact on research community",
			description: "Build tools that directly empower researchers worldwide to accelerate their groundbreaking work.",
			icon: IconGlobe
		},
		{
			title: "Continuous learning environment",
			description: "Stay ahead of rapidly evolving AI technologies with dedicated learning time, conference attendance, and research collaboration.",
			icon: IconUsers
		}
	];

	const openings: JobOpening[] = [
		// AI & Research
		{
			title: "Senior AI Research Engineer",
			department: "Research",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Machine Learning Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Research Scientist - NLP",
			department: "Research",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "AI Platform Engineer",
			department: "Engineering",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Product & Design
		{
			title: "Research UX Designer",
			department: "Design",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "AI Product Manager",
			department: "Product",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},

		// Business & Partnerships
		{
			title: "Research Partnerships Manager",
			department: "Business Development",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Academic Relations Coordinator",
			department: "Business Development",
			location: "Remote",
			type: "Full-time",
			url: "#"
		},
		{
			title: "Technical Writer - AI Documentation",
			department: "Content",
			location: "Remote",
			type: "Full-time",
			url: "#"
		}
	];

	const employeeTestimonials = [
		{
			name: "Dr. Priya Sharma",
			position: "Senior Research Scientist",
			company: "Core AI Team",
			quote:
				"I've grown more here in six months than I did in two years at my last lab. Working on tools that I actually would've wanted during my PhD is incredibly fulfilling.",
			image:
				"/generated/image-a-professional-portrait-of-an-indian-wom.webp"
		},
		{
			name: "Alex Johnson",
			position: "Machine Learning Engineer",
			company: "Infrastructure and Data",
			quote:
				"Everyone here cares deeply about the scientific process, not just the tech. We're solving real research problems—not chasing hype. That's why I joined and why I'm staying.",
			image:
				"/generated/image-a-professional-portrait-of-a-young-black.webp"
		},
		{
			name: "Maria Santos",
			position: "Product Manager",
			company: "Research Tools",
			quote:
				"It's rare to ship AI-enabled features for actual researchers and see them used a week later by a university immunology team. That kind of impact doesn't get old.",
			image:
				"/generated/image-a-professional-portrait-of-a-latina-woma.webp"
		}
	];

	const processSteps = [
		{
			step: 1,
			title: "Apply",
			description:
				"Submit your application with your resume, portfolio, and any relevant research papers or AI projects you've worked on."
		},
		{
			step: 2,
			title: "Technical assessment",
			description: "Participate in a technical discussion about AI concepts and collaborate on a small research problem with our team."
		},
		{
			step: 3,
			title: "Cultural fit & vision",
			description: "Meet with team members to discuss your passion for research impact and alignment with our mission."
		},
		{
			step: 4,
			title: "Welcome aboard",
			description: "Join our research-focused team and start contributing to AI solutions that advance scientific discovery."
		}
	];

	const values = [
		{
			icon: IconHeart,
			title: "Research-driven innovation",
			description: "We're passionate about pushing the boundaries of what's possible with AI to solve real research challenges."
		},
		{
			icon: IconUsers,
			title: "Scientific collaboration",
			description: "We work closely with researchers across disciplines, fostering an environment of shared knowledge and discovery."
		},
		{
			icon: IconGlobe,
			title: "Accelerating discovery",
			description: "Our mission is to democratize AI tools, enabling researchers worldwide to make breakthrough discoveries faster."
		}
	];
</script>

<!-- Hero Section -->

<SecondaryHero
	title="Shape the future of AI for researchers"
	subtitle="Join a passionate team building cutting-edge AI solutions that empower researchers worldwide. Be part of something that advances human knowledge and discovery."
	imageSrc="/generated/image-a-diverse-team-of-researchers-gathered-a.webp"
/>

<!-- Why Join Us Section -->
<section class={SECTION_BASE_CLASSES}>
	<SectionHeader title="Why join us?" subtitle="Build your career while making an impact" />

	<div class="mt-16 grid gap-4 md:grid-cols-3">
		{#each benefits as benefit}
			<Card {...benefit} />
		{/each}
	</div>
</section>

<!-- Culture Section -->
<Culture {values} />

<Testimonials testimonials={employeeTestimonials} />

<!-- Application Process -->
<section class={SECTION_BASE_CLASSES}>
	<div class="mx-auto">
		<h2 class="text-title1 mb-16">Our application process</h2>

		<div class="grid gap-12 md:grid-cols-2 lg:grid-cols-4">
			{#each processSteps as { step, title, description }, i}
				<div class="flex flex-col">
					<div class="{ICON_CONTAINER_CLASSES} mb-6 size-11">
						<span class="text-headline">{step}</span>
					</div>
					<h3 class="text-headline mb-3">{title}</h3>
					<p class="text-body text-emphasis-low">{description}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
<!-- Current Openings Section -->
<section class={GRADIENT_BG_CLASSES}>
	<div class="section-px section-py container mx-auto grid w-full items-start lg:grid-cols-2">
		<SectionHeader title="Current openings" subtitle="Find your perfect role" />

		<JobList {openings} />
	</div>
</section>
