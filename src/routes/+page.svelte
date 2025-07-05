<script lang="ts">
	// Components
	import Summary from "$lib/components/layout/Summary.svelte";
	import Features from "$lib/components/layout/Features.svelte";
	import Testimonials from "$lib/components/layout/Testimonials.svelte";
	import CallToAction from "$lib/components/layout/CallToAction.svelte";
	import AboutTeaser from "$lib/components/layout/AboutTeaser.svelte";
	import LogoScroller from "$lib/components/layout/LogoScroller.svelte";
	import CenteredTextOnlyHero from "$lib/components/layout/hero-sections/CenteredTextOnlyHero.svelte";
	import UseCases from "$lib/components/layout/UseCases.svelte";
</script>

<CenteredTextOnlyHero
	title="Research isn't the hard part"
	subtitle="Focus on the thinking—let Anara handle the rest."
	imageSrc="/generated/image-a-serene-coastal-landscape-at-dawn-with-.webp"
/>
<LogoScroller 
	label="Trusted by leading research organizations"
	logoUrls={[
		'https://logo.clearbit.com/mit.edu',
		'https://logo.clearbit.com/stanford.edu',
		'https://logo.clearbit.com/pfizer.com',
		'https://logo.clearbit.com/novartis.com'
	]}
/>

<Summary
	title="What we do"
	text="Anara develops AI solutions specifically designed to assist researchers across various fields. We help researchers leverage AI to enhance their work, letting them focus on the thinking while we handle the rest."
/>

<Testimonials
	testimonials={[
		{
			name: "Dr. Cordelia Blackwood",
			position: "Senior Research Scientist",
			company: "Cambridge Biomedical Institute",
			quote:
				"Anara reduced our data analysis time from weeks to days. What used to take our team 3 weeks of manual processing now happens in 4 days.\nWe've accelerated our publication timeline by 40% while maintaining rigorous standards.",
			image:
				"/generated/image-a-professional-female-researcher-in-a-mo.webp"
		},
		{
			name: "Dr. Thaddeus Voss",
			position: "Principal Investigator",
			company: "Max Planck Institute",
			quote:
				"Before Anara, we lost $180,000 on a failed experiment due to overlooked literature. Their AI caught contradictory findings we missed.\nNow we validate our hypotheses against the entire research landscape before investing resources.",
			image:
				"/generated/image-a-male-scientist-working-diligently-in-a.webp"
		},
		{
			name: "Zara Okafor",
			position: "PhD Candidate",
			company: "University of Edinburgh",
			quote:
				"Anara saved me $15,000 in research costs by identifying existing datasets that matched my needs perfectly.\nI avoided duplicating expensive experiments and finished my dissertation 6 months ahead of schedule.",
			image:
				"/generated/image-a-female-phd-student-in-a-university-res.webp"
		}
	]}
/>

<Features
	title="AI built for researchers"
	subtitle="Anara helps researchers go further, faster—without the busywork"
	features={[
		{
			title: "Do more in less time",
			description: "Anara automates research tasks like literature reviews, data annotation, experiment tracking, and more. Spend less time managing, more time thinking."
		},
		{
			title: "Your second brain for research",
			description: "Upload papers, notes, and datasets. Anara extracts insights, builds connections, and even drafts hypothesis-driven reports based on your materials."
		},
		{
			title: "Stay in your flow",
			description: "Ask questions in plain language. Anara finds answers, traces sources, and shows its work."
		},
		{
			title: "Works across domains",
			description: "Whether you're in biology, social science, computer science or beyond—Anara is trained on interdisciplinary models built to support real academic research."
		},
		{
			title: "Built by and for researchers",
			description: "We're researchers too. We know what it's like to dig through text files at 2am."
		},
		{
			title: "Ready to accelerate your work",
			description: "Try Anara free—no setup, no fluff. Just faster, smarter research."
		}
	]}
/>

<UseCases
	title="Use cases"
	subtitle="Real-world applications for research teams"
	useCases={[
		{
			title: "Accelerate academic reviews",
			description: "Cut hours off your literature review process by letting Anara summarize, extract, and link critical insights across hundreds of papers. Ideal for thesis work or grant prep.",
			image: "/generated/image-a-diverse-group-of-academic-researchers-.webp",
			link: {
				href: "/use-cases/academic-reviews",
				label: "Learn more"
			}
		},
		{
			title: "Improve clinical research speed and accuracy",
			description: "In biomedical fields, Anara extracts peer-reviewed findings and tracks evolving hypotheses—reducing manual error and surfacing key data faster.",
			image: "/generated/image-a-team-of-medical-researchers-in-a-clini.webp",
			link: {
				href: "/use-cases/clinical-research",
				label: "Learn more"
			}
		},
		{
			title: "Streamline data-driven research",
			description: "For data scientists and technical researchers, Anara interprets model documentation, automates technical summarization, and helps synthesize across datasets.",
			image: "/generated/image-a-group-of-data-scientists-in-a-modern-o.webp",
			link: {
				href: "/use-cases/data-driven-research",
				label: "Learn more"
			}
		}
	]}
/>

<AboutTeaser />
<CallToAction />
