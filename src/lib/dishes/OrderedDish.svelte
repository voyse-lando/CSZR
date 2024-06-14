<script>
    import { Accordion, AccordionItem, Card, List, Li, Toggle } from "flowbite-svelte";
 
	/** @type {string} */
	export let img;
	/** @type {string} */
	export let name;

	/** @type {string[]}*/
	export let ingredients = [];

	/** @type {boolean} */
	export let ready = false;
</script>

<Card class="{ready ? "dark:bg-gradient-to-bl" : ""} from-primary-900 to-gray-800" {img}>
	<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
		{name}
	</h5>
	<Toggle bind:checked={ready} class="dark:text-white {ready ? "" : "italic"}">{ready ? "Gotowe" : "W trakcie przygotowania" }</Toggle>
	<Accordion class="mt-6">
		<AccordionItem>
			<span slot="header">Składniki</span>
			<List>
				{#each ingredients as i }
					<Li>{i}</Li>
				{/each}
			</List>
		</AccordionItem>
	</Accordion>
</Card>