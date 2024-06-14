<script>
    import { Card } from "flowbite-svelte";

	/** @type {number} */
	export let id;
	/** @type {boolean} */
	export let done = false;

	const cardClass = done ? "dark:bg-gradient-to-tl from-primary-900" : "";
	const headingClass = "mb-2 text-center text-6xl font-bold tracking-tight text-gray-900 dark:text-white";
	const descClass = done ? "dark:text-white font-bold" : "dark:text-gray-400"
</script>


<Card class={cardClass} href="/zamowienia/{id}">
	<h2 class={headingClass}>
		{id}
	</h2>
	<p class={descClass}>{done ? "Gotowe" : "W trakcie przygotowywania"}</p>
</Card>