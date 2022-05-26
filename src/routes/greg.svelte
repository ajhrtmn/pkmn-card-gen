<script context="module">
	export const prerender = true;
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<!--  --><!--  --><!--  --><!--  --><!--  --><!--  -->
<!--  --><!--  --><!--  --><!--  --><!--  --><!--  -->


<script>
	// The Card itself X
	// Yellow border X
	// Content container: gradient background
	// Content Grid
	// Header: Evolution info, instructionals, name, hp, type, Prevolution Section
	// // Prevolution Circle area, small avatar, stage level
	// Avatar: Sprite, background image, border, dropshadow
	// Caption: details, generation icon
	// Move List: Type cost, name, descriptions, damage
	// Negatives: weakness types, resistance, retreat cost
	// Footer: Text(italic) and border
	// Artist/copyright
</script>


<section class="w-full flex items-center justify-center bg-gray-500">
	<div class="p-3 bg-yellow-200 rounded-xl shadow-lg">
		
		
		<div id="container">

			<div id="header">
				<div id="evolution" class="grid grid-cols-2 gap-3 p-2">
					<div class="text-xs font-semibold italic">Evolves from Growithe</div>
					<div class="text-xs ">Put Arcanine on the Basic Pokémon</div>
				</div><!-- id="evolution" -->

				<div class="w-11/12 mx-auto pt-1 bg-yellow-200"></div>

				<div id="vitals" class="p-2 grid grid-cols-12 gap-2">
					<div id="name" class="col-span-7 font-semibold text-lg">Arcanine</div>
					<div id="hp" class="col-span-3 text-white font-semibold">100 HP</div>
					<div id="type" class="col-span-2">FIRE</div>
				</div><!-- id="vitals" -->
			</div><!-- id="header" -->
			<div id="avatar" class="flex items-center justify-center">
				<img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/59.svg" alt="Arcanine on Meadow"/>
			</div><!-- id="avatar" -->
		</div><!-- id="container" -->

	</div>
</section>


<style>
	section {
		min-height: 100vh;
	}

	#avatar {
		border-width: .25rem;
		border-style: solid;
		border-color: yellow;
		margin: 0 1rem;
		aspect-ratio: 4/3;
		background-size: cover;
		background-image: url('https://images.unsplash.com/photo-1470240731273-7821a6eeb6bd?crop=entropy&cs=tinysrgb&fm=jpg&ixlib=rb-1.2.1&q=80&raw_url=true&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470');
	}

	#avatar > img {
		max-width: 85%;
		max-height: 90%;
		transform: scaleX(-1);
	}

	#container {
		width: 300px;
		height: 500px;
		color: #000000;
		background-color: rgba(207, 29, 29, 1);
	}

	.italic { font-style: italic; }
</style>
