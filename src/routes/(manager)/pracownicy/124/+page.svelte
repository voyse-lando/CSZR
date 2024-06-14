<script>
    import { Accordion, AccordionItem, Avatar, Badge, Button, Card, Hr, Input, Label, Li, List, Select } from "flowbite-svelte";

	const positions = [
		{ value: "cook", name: "Kucharz" },
		{ value: "cashier", name: "Pracownik obsługi" },
		{ value: "delivery", name: "Dostawca" },
	];
</script>

<style>
	.panel {
		padding-inline: clamp(5rem, 10%, 20rem);
	}
</style>

<div class="panel p-8 ml-auto flex">
	<Card class="mr-auto ml-auto flex min-w-full items-center">
		<Avatar size="lg" class="mr-auto ml-auto mb-8" />
		<h3 class="mb-4 text-center text-4xl font-extrabold dark:text-white md:text-5xl lg:text-6xl">
			Jan Kowalski
		</h3>
		<Badge class="text-xl">Kucharz</Badge>
		<Hr classHr="w-7/12 h-1 mx-auto my-4 rounded md:my-10" />
		<Accordion multiple class="w-1/2">
			<AccordionItem open>
				<span slot="header">Informacje ogólne</span>
				<List list="none">
					<Li>Pracuje od: 12.04.2020</Li>
					<Li>Wynagrodzenie: 4550.30 zł</Li>
				</List>
			</AccordionItem>
			<AccordionItem open>
				<span slot="header">Edycja</span>
				<div class="grid grid-cols-2 max-md:grid-cols-1 gap-8" >
					<div>
						<div class="mb-4">
							<Label for="firstname">Imię:</Label>
							<Input id="firstname" placeholder="<<bez zmian>>" />
						</div>
						<div class="mb-4">
							<Label for="lastname">Nazwisko:</Label>
							<Input id="lastname" placeholder="<<bez zmian>>" />
						</div>
						<Button class="mb-4">Zmień dane</Button>
					</div>
					<div>
						<div class="mb-4">
							<Label for="position">Stanowisko:</Label>
							<Select id="position" placeholder="<<bez zmian>>" items={positions} />
						</div>
						<Button>Zmień stanowisko</Button>
					</div>
				</div>
			</AccordionItem>
		</Accordion>
	</Card>
</div>