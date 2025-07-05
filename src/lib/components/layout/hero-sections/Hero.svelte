<!--
    @component
    Sleek, minimal hero banner optimized for AI research company. Clean typography and focused messaging.

    Usage:
    ```html
    <Hero
      title="AI built for research"
      subtitle="Tools made for researchers, not just data"
      imageSrc="/hero.jpg"
      callsToAction={[
        {
          href: "/start",
          label: "Get started"
        }
      ]}
    />
    ```

    Props:
    - `title`: Main headline (string)
    - `subtitle`: Supporting text (string)
    - `imageSrc`: Hero image URL (string)
    - `callsToAction`: CTA buttons array (max two: primary, secondary)
-->

<script lang="ts">
	// Components
	import Button from "$lib/components/ui/Button.svelte";

	// Constants
	import { cta } from "$lib/navigation";

	function handleImageError(e: Event) {
		const target = e.currentTarget as HTMLImageElement;
		target.src = "https://placehold.co/800x600/f8fafc/64748b?text=Hero+image";
	}

	// Types
	type Props = {
		title: string;
		subtitle: string;
		imageSrc?: string;
		callsToAction?: Array<{
			href: string;
			label: string;
		}>;
	};

	let {
		title,
		subtitle,
		imageSrc,
		callsToAction = [cta],
		...rest
	}: Props = $props();
</script>

<section class="bg-background" {...rest}>
	<div class="section-px container mx-auto">
		<!-- Hero Content -->
		<div class="grid gap-12 py-20 lg:grid-cols-2 lg:items-center lg:gap-16">
			<!-- Text Content -->
			<div class="space-y-8">
				<div class="space-y-4">
					<h1 class="text-display text-balance leading-tight">
						{title}
					</h1>
					<p class="text-headline text-muted-foreground max-w-[50ch]">
						{subtitle}
					</p>
				</div>

				{#if callsToAction.length > 0}
					<div class="flex gap-4">
						{#each callsToAction as cta, index}
							<Button
								href={cta.href}
								size="lg"
								variant={index % 2 === 0 ? "primary" : "secondary"}
								class="transition-all duration-200 hover:scale-105"
							>
								{cta.label}
							</Button>
						{/each}
					</div>
				{/if}
			</div>

			<!-- Image -->
			{#if imageSrc}
				<div class="relative">
					<div class="aspect-[4/3] overflow-hidden rounded-lg border border-border">
						<img
							src={imageSrc}
							alt="Research team collaborating with AI tools"
							class="size-full object-cover transition-transform duration-300 hover:scale-105"
							onerror={handleImageError}
						/>
					</div>
				</div>
			{/if}
		</div>
	</div>
</section>
