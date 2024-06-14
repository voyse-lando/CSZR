<script>
    import { Navbar, NavBrand, NavHamburger, NavUl, Avatar } from "flowbite-svelte";
	import "../../app.css";
</script>

<Navbar>
	<NavBrand href="/">
		<span class="self-center whitespace-nowrap text-4xl font-semibold dark:text-white">CSZR</span>
	</NavBrand>
	<NavHamburger />
	<NavUl>
	</NavUl>
	<div class="flex items-center space-x-4 rtl:space-x-reverse">
		<Avatar>JK</Avatar>
		<div class="space-y-1 font-medium dark:text-white">
		  <div>Jan Kowalski</div>
		  <div class="text-sm text-gray-500 dark:text-gray-400">Kucharz</div>
		</div>
	</div>
</Navbar>
<slot />