<script>
    import { Button, Card, Heading, Toggle } from "flowbite-svelte";
	import { CloseOutline } from "flowbite-svelte-icons"
	import OrderedDish from "$lib/dishes/OrderedDish.svelte";

	let vc1 = false, vc2 = true;

	const pepperoniIng = [
		"Ciasto",
		"Ser Mozzarella",
		"Sos Pomidorowy",
		"Pepperoni"
	];
	const cesarIng = [
		"Sałata",
		"Pomidor",
		"Sos vinaigrette",
		"Kurczak"
	];
</script>

<div class="p-16 flex flex-col">
	<Button href="/zamowienia" pill class="ml-auto !p-2"><CloseOutline size="xl" /></Button>
	<Heading tag="h1" class="mb-4 text-center" customSize="text-4xl font-extrabold  md:text-5xl lg:text-6xl">
		Zarządzanie zamówieniem #42
	</Heading>
	<div class="p-8 flex flex-wrap justify-center items-center gap-4">
		<OrderedDish img="/pepperoni.jpg" name="Pizza Pepperoni" ingredients={pepperoniIng}  bind:ready={vc1} />
		<OrderedDish img="/cezar.jpg" name="Sałatka Cezar" ingredients={cesarIng} bind:ready={vc2} />
	</div>
	<Button disabled={!(vc1 && vc2)} class="ml-auto mr-auto text-xl">Wydaj zamówienie</Button>
</div>