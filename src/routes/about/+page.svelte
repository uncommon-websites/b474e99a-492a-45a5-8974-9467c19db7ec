<script lang="ts">
	// Components
	import CallToAction from "$lib/components/layout/CallToAction.svelte";

	// Icons
	import StakeholderGrid from "$lib/components/layout/StakeholderGrid.svelte";
	import Story from "./Story.svelte";
	import SecondaryHero from "$lib/components/layout/hero-sections/SecondaryHero.svelte";
	import Culture from "$lib/components/layout/Culture.svelte";

	// Constants
	const values = [
		{
			title: "Research-first design",
			description: "Every feature we build starts with understanding real researcher workflows and pain points."
		},
		{
			title: "Augmentation over automation",
			description: "We believe AI should amplify human intelligence, not replace the critical thinking that drives discovery."
		},
		{
			title: "Open collaboration",
			description: "Knowledge grows when shared. We build tools that enhance collaboration across research communities."
		}
	];
</script>

<SecondaryHero
	title="Empowering research"
	subtitle="through artificial intelligence"
	imageSrc="/generated/image-a-diverse-group-of-researchers-collabora.webp"
/>

<!-- Story Section -->
<Story
	paragraphs={[
		"Research has always been the engine of human progress, but researchers today face an overwhelming amount of data and complexity. We founded Anara with a simple mission: create AI solutions that amplify human intelligence, not replace it.",
		"Every day, brilliant minds across universities and institutions struggle with time-consuming tasks that pull them away from what they do best—discovering, analyzing, and innovating. Our AI tools are designed to handle the heavy lifting, giving researchers more time to focus on breakthrough thinking.",
		"We believe that when AI serves researchers effectively, it accelerates the pace of discovery for everyone. From faster literature reviews to intelligent data analysis, Anara is building the future where technology empowers the people pushing the boundaries of human knowledge."
	]}
/>

<!-- Our Culture Section -->
<Culture {values} />

<!-- StakeholderGrid Section -->
<StakeholderGrid
	stakeholderType="team"
	title="Meet our founder."
	subtitle="Leading AI innovation for researchers."
	stakeholders={[
		{
			name: "Naveed",
			position: "Founder & CEO",
			bio: "Passionate about empowering researchers with AI tools that amplify human intelligence and accelerate discovery.",
			image: "/generated/image-a-professional-headshot-of-a-male-founde.webp"
		}
	]}
/>

<!-- CTA Section -->
<CallToAction />
