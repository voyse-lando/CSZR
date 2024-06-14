<script>
    import { Heading, Card, Toggle, Button } from "flowbite-svelte";
	import Order from "$lib/orders/Order.svelte"
</script>

<div class="p-8 flex flex-col">
	<Heading tag="h1" class="mb-4 text-center" customSize="text-4xl font-extrabold  md:text-5xl lg:text-6xl">
		Zarządzanie zamówieniami
	</Heading>
	<div class="ml-16 mr-16 p-16 flex flex-wrap justify-center items-center gap-4">
		<Order id={41} />
		<Order id={42} />
		<Order id={44} done />
		<Order id={45} done />
		<Order id={47} />
		<Order id={48} />
		<Order id={49} />
	</div>
</div>