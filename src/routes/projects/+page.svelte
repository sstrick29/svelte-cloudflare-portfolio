<script>
	
    const projects = [
	{
		title: 'GDLauncher',
		technologies: ['Node', 'React', 'Redux', 'Electron'],
		description:
			'GDLauncher is a simple, yet powerful Minecraft custom launcher with a strong focus on the user experience',
		url: 'https://github.com/gorilla-devs/GDLauncher'
	},
	{
		title: 'WiseMan Discord Bot',
		technologies: ['NodeJs', 'FireBase', 'MongoDb', 'golang'],
		description:
			'The wiseMan bot allows you to level up based on the time you spend in a vocal channel',
		url: 'https://github.com/Ladvace/WiseMan-DiscordBot'
	},

];

</script>

<svelte:head>
	<title>Gianmarco Cavallo — Projects</title>
</svelte:head>

<div class="projectContainer">
	<div class="projects">
		<h1>Projects</h1>
		<p class="note">
			Note: most of my projects are under NDA so I am unable to share those projects. If there is
			anything you would like to see further, please feel free to contact me.
		</p>
		{#each projects as project}
			<div class="project">
				<div class="header">
					<h2>
						{project.title}
					</h2>
					<div class="techsContainer">
						Technologies:
						<div class="techs">
							{#each project.technologies as tech}
								<div>{tech}</div>
							{/each}
						</div>
					</div>
				</div>
				<p>
					{project.description}
				</p>
				<a href={project.url} target="_blank" rel="noreferrer">
					<div class="button">Project url =></div>
				</a>
			</div>
		{/each}
	</div>
</div>