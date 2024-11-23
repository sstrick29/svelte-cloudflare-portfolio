<script>
	
    const projects = [
	{
		title: '32 bit CPU ',
		technologies: ['Verilog/SVerilog', 'Python', 'cocotb', 'Electron'],
		description:
			'A simple yet powerful 32 bit cpu written in Verilog/System Verilog. Tested using cocotb in Python.',
		url: 'https://github.com/sstrick29/ale81-32bit-cpu.git'
	},
	{
		title: 'Digital Geiger-Muller Counter',
		technologies: ['C', 'C++', 'Altium', 'PSpice'],
		description:
			'This project compines microcontroller programming with circuit design.',
		url: 'https://github.com/sstrick29/GMcounter-pico-digital.git'
	},
    {
		title: 'Handwritten Digits Image Recognition',
		technologies: ['Python', 'Linux', 'OpenGL', 'Machine Learning'],
		description:
			'This project integrates computer vision with machine learning to read and predict handwritten digits.',
		url: 'https://github.com/sstrick29/mnist-TF-computervision-Rpi4.git'
	},
    {
		title: 'Portfolio Website',
		technologies: ['Node.js', 'Svelte.js', 'Cloudflare Infrastructure', ''],
		description:
			'This projects represents what I know about building web-based applications and deploying to live web services. You can find it deployed here.',
		url: 'https://github.com/sstrick29/svelte-cloudflare-portfolio.git'
	},
    

];

</script>

<svelte:head>
	<title>Samuel Strickland — Projects</title>
</svelte:head>

<div class="projectContainer">
	<div class="projects">
		<h1>Projects</h1>
		<p class="note">
			These are a collection of projects I'd like to showcase.
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
					<div class="button">Project code</div>
				</a>
			</div>
		{/each}
	</div>
</div>