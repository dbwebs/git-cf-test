<script>
    const veg = '/images/health/veggie-pic.jpg';

    const h = [
		{
			title: "Health through Nutrition and Exercise",
			description: 'Our take on the importance of a good diet balanced with exercise',
			src: veg,
			href: '/articles/health'
		}
	];

	const list = [
		{ name: 'Health Articles', abbr: h }
	];
</script>

<section id="articles" class="p-5">
    <h1 class="text-light">List of Articles</h1>
    <p class="text-light">Here we talk about topics that are important to us and our great experiences</p>

    <hr class="text-light" />
	{#each list as li}
		<h1 class="text-light text-center">{li.name}</h1>
		<div class="row">
			{#each li.abbr as p}
				<div class="col-md-4 py-3 mw-600 mx-auto">
					<div class="card">
						<img class="card-img-top" src={p.src} alt={p.title} />
						<div class="card-body">
							<h4 class="card-title">{p.title}</h4>
							<p class="card-text">
								{p.description}
							</p>
							{#if p.href !== ''}
								<a href={p.href} class="btn btn-primary">Learn more</a>
							{/if}
						</div>
					</div>
				</div>
			{/each}
		</div>
		<hr class="text-light" />
	{/each}
</section>