<script>
    import { Avatar, Button, Card, Heading, Helper, Input } from "flowbite-svelte";

</script>

<div class="p-8 flex flex-col">
	<Heading tag="h1" class="mb-4 text-center" customSize="text-4xl font-extrabold  md:text-5xl lg:text-6xl">
		Zaloguj się
	</Heading>
	<Card class="mr-auto ml-auto p-8">
		<Avatar class="mb-6 mr-auto ml-auto" size="lg" ></Avatar>
		<div class="mb-6">
			<Input id="large-input" type="email" size="lg" placeholder="E-Mail" />
		</div>
		<div class="mb-6">
			<Input id="large-input" type="password" size="lg" placeholder="Hasło" />
		</div>
		<div class="mb-6 flex">
			<Button class="ml-auto mr-auto text-lg">
				<span class="pr-4 pl-4">
					Zaloguj się
				</span>
			</Button>
		</div>
	</Card>
</div>