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

				<div id="vitals" class="py-1 grid grid-cols-2 gap-2 items-baseline relative z10">
					<div id="name" class="col-span-1 font-bold text-xl">
						<div class="">Arcanine</div>
					</div>
					<div class="col-span-1 flex flex-row gap-2 items-end justify-end">
						<div id="hp" class="col-span-4 text-red-600 font-bold text-lg text-right">100 HP</div>
						<div id="type" class="col-span-2 flex flex-col items-end">
							<div class="bg-red-500 type-icon flex items-center justify-center">
								<span class="material-icons text-black-500">local_fire_department</span>
							</div>
						</div>
					</div>
				</div><!-- id="vitals" -->

			</div><!-- id="header" -->


			<div id="avatar" class="flex items-center justify-center relative z10">
				<img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/59.svg" alt="Arcanine on Meadow"/>
			</div><!-- id="avatar" -->





			<img class="card-bg" src="https://images.unsplash.com/photo-1519145127298-00d5287fcdd3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8NHx8Z3J1bmdlfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="">
		</div><!-- id="container" -->
	</div>
</section>


<style>
	section {
		background-image: url('https://images.unsplash.com/photo-1613771404784-3a5686aa2be3?ixlib=rb-1.2.1&raw_url=true&q=80&fm=jpg&crop=entropy&cs=tinysrgb&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169');
		background-size: cover;
		position: relative;
		min-height: 100vh;
		padding: 4px;
	}

	.card-bg {
		opacity: .25;
		position: absolute; top: 0; object-fit: cover;
		width: 400px; height: 560px;
		mix-blend-mode: lighten;
		filter: grayscale(100%);
	}

	#name { transform: scaleX(1.125); }
	#name, #hp { transform: scaleY(1.4); }

	#avatar > img { max-width: 85%; height: 85%; transform: scaleX(-1); }
	#avatar {
		border-width: .5rem; border-style: solid;
		border-color: rgba(234,210,3,1);
		margin: 4px 1.5rem;
		aspect-ratio: 4/3;
		box-shadow: 5px 5px 15px 5px rgba(0, 0, 0, 0.493);
		background-size: cover;
		background-image: url('https://images.unsplash.com/photo-1470240731273-7821a6eeb6bd?crop=entropy&cs=tinysrgb&fm=jpg&ixlib=rb-1.2.1&q=80&raw_url=true&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470');
	}

	#container {
		width: 90vw;
		max-width: 400px;
		aspect-ratio: 1/1.4;
		color: #000000;
		overflow: hidden;
		background-color: rgba(207, 29, 29, 1);
		background-image: linear-gradient(45deg, rgb(175, 1, 1), rgb(214, 159, 75),rgb(224, 151, 121));
	}
	#vitals {
		position: relative;
		bottom: 10px;
		margin: 2px 1rem;
		margin-bottom: -10px;
	}

	.type-icon {
		margin: 0; padding: 0;
		height: 35px; width: 35px;
		border-radius: 50%;
	}

	
</style>
