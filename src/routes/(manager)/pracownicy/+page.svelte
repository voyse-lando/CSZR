<script>
	import { Accordion, AccordionItem, Avatar, Button, Card, Heading } from 'flowbite-svelte';

	const kucharze = [
		"Wojciech Nowak",
		"Jan Kowalski",
		"Karol Dawid"
	];
	const obsluga = [
		"Edward Rzecki",
		"Andrzej Lewandowski",
		"Joanna Wielicka",
		"Katarzyna Budeń"
	];
	const dostawcy = [
		"Edward Rzecki",
		"Anna Jakubowska"
	];
</script>

<div class="p-8 flex flex-col">
	<Heading tag="h1" class="mb-4 text-center" customSize="text-4xl font-extrabold  md:text-5xl lg:text-6xl">
		Zarządzanie pracownikami
	</Heading>
	<div class="flex flex-row gap-8 justify-center max-w-12xl ml-auto mr-auto pb-16">
		<Card>
			<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
				Kucharze
			</h5>
			<Accordion>
				{#each kucharze as p}
				<AccordionItem >
					<span class="dark:text-white" slot="header">{p}</span>
					<Button href="/pracownicy/124" outline>Edytuj</Button>
				</AccordionItem>
				{/each}
			</Accordion>
		</Card>
		<Card>
			<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
				Pracownicy obsługi
			</h5>
			<Accordion>
				{#each obsluga as p}
				<AccordionItem >
					<span class="dark:text-white" slot="header">{p}</span>
					<Button outline>Edytuj</Button>
				</AccordionItem>
				{/each}
			</Accordion>
		</Card>
		<Card>
			<h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">
				Dostawcy
			</h5>
			<Accordion>
				{#each dostawcy as p}
				<AccordionItem >
					<span class="dark:text-white" slot="header">{p}</span>
					<Button outline>Edytuj</Button>
				</AccordionItem>
				{/each}
			</Accordion>
		</Card>
	</div>
</div>