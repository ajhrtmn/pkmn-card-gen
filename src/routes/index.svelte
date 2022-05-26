<script context="module">
	export const prerender = true;
</script>

<svelte:head>
	<title>Pokemon Card Generator - Practice Project</title>
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


<section class="w-full flex items-center justify-center bg-gray-500 font-montserrat">
	<div class="p-3 bg-pkmn-card-yellow rounded-xl shadow-lg relative">
		
		
		<div id="container" class="relative">
			<div id="header" class="mx-2 relative z10">
				<div id="evolution" class="grid grid-cols-2 gap-3 p-2 relative z10">
					<!-- <div class="text-xs font-semibold italic">Evolves from Growithe</div>
					<div class="text-xs ">Put Arcanine on the Basic Pokémon</div> -->
				</div><!-- id="evolution" -->

				<!-- <div class="w-11/12 mx-auto bg-pkmn-card-yellow divider"></div> -->

				<div id="vitals" class="p-2 grid grid-cols-12 gap-2 items-baseline relative z10">
					<div id="name" class="col-span-6 font-bold text-xl">
						<div class="">Arcanine</div>
					</div>
					<div id="hp" class="col-span-4 text-red-600 font-bold text-lg text-right">100 HP</div>
					<div id="type" class="col-span-2">
						<div class="bg-red-500 type-icon flex items-center justify-center">
							<span class="material-icons text-black-500">local_fire_department</span>
						</div>
					</div>
				</div><!-- id="vitals" -->

			</div><!-- id="header" -->


			<div id="avatar" class="flex items-center justify-center relative z10">
				<img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/59.svg" alt="Arcanine on Meadow"/>
			</div><!-- id="avatar" -->





			<img class="fire-bg" src="https://images.unsplash.com/photo-1543005472-1b1d37fa4eae?crop=entropy&cs=tinysrgb&fm=jpg&ixlib=rb-1.2.1&q=80&raw_url=true&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=687" alt="">
		</div><!-- id="container" -->
	</div>
</section>


<style>
	section {
		background-image: url('https://images.unsplash.com/photo-1613771404784-3a5686aa2be3?ixlib=rb-1.2.1&raw_url=true&q=80&fm=jpg&crop=entropy&cs=tinysrgb&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169');
		background-size: cover;
		position: relative;
		min-height: 100vh;
	}

	.fire-bg {
		opacity: .35;
		position: absolute; top: 0; object-fit: cover;
		width: 300px; height: 500px;
	}

	#name > div { transform: scaleX(.8); margin-left: -10%; }
	#name, #hp { transform: scaleY(1.3); }

	#avatar > img { max-width: 85%; max-height: 85%; transform: scaleX(-1); }
	#avatar {
		border-width: .33rem; border-style: solid;
		border-color: rgba(234,210,3,1);
		margin: 0 1rem;
		aspect-ratio: 4/3;
		box-shadow: 5px 5px 15px 5px rgba(0, 0, 0, 0.493);
		background-size: cover;
		background-image: url('https://images.unsplash.com/photo-1470240731273-7821a6eeb6bd?crop=entropy&cs=tinysrgb&fm=jpg&ixlib=rb-1.2.1&q=80&raw_url=true&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470');
	}

	#container {
		width: 300px; height: 500px;
		color: #000000;
		overflow: hidden;
		background-color: rgba(207, 29, 29, 1);
		background-image: linear-gradient(45deg, rgba(207, 29, 29, 1), rgb(211, 201, 109), white);;
	}
	#vitals {
		position: relative;
		bottom: 15px;
		margin-bottom: -15px;
	}

	.type-icon {
		margin: 0; padding: 0;
		height: 35px; width: 35px;
		border-radius: 50%;
	}

	
</style>
