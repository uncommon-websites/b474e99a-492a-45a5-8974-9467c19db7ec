<script lang="ts">
	// Types
	import type { PageProps } from "./$types";

	// Components
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import Pricing from "$lib/components/layout/Pricing.svelte";

	// Props
	const { data }: PageProps = $props();
</script>

<Pricing />

<Testimonials
	testimonials={[
		{
			name: "Dr. Lena Aboudine",
			position: "Clinical Research Lead",
			company: "Carysis Labs",
			quote:
				"With Anara, I'm able to extract the core ideas from technical papers in minutes instead of hours. It's become essential to how I work.",
			image: "/generated/image-a-professional-headshot-of-dr-lena-aboud.webp"
		},
		{
			name: "Marcel Grohn",
			position: "Applied Policy Researcher",
			company: "Praxis Insights",
			quote:
				"It's like getting a second-brain that understands academic reasoning. I don't write anything serious without it now.",
			image: "/generated/image-a-professional-headshot-of-marcel-grohn-.webp"
		},
		{
			name: "Serena Chong",
			position: "PhD Candidate",
			company: "University of Edinburgh",
			quote:
				"Anara handles the tedious context-switching in my literature reviews so I can stay focused on discovery and synthesis.",
			image: "/generated/image-a-professional-headshot-of-serena-chong-.webp"
		}
	]}
/>

<CallToAction 
	title="Ready in minutes"
	subtitle="Get started now"
	description="Your time is better spent thinking than typing. Start using Anara instantly—no setup, no integration, no tutorials needed. See what purpose-built AI for researchers can do for you today."
	imageSrc="/generated/image-a-joyful-researcher-sitting-at-a-desk-su.webp"
	callsToAction={[
		{
			href: "/signup",
			label: "Start free trial",
			variant: "primary"
		},
		{
			href: "/demo",
			label: "Book a demo",
			variant: "secondary"
		}
	]}
/>
