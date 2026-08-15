<article class="flex max-h-96 flex-col items-start justify-center gap-4">
	<div>
		<div class="flex flex-wrap items-center justify-start gap-2 gap-y-0">
			<h1 class="text-lg text-white">Undergraduate Research Fellow</h1>
			<h1 class="text-lg text-cyan-500">@</h1>
			<button
				on:click={() => window.open('https://culair.weebly.com/')}
				class="cursor-pointer text-left text-lg text-cyan-500 hover:underline"
			>
				Colorado Center for Astrodynamics Research
			</button>
		</div>
		<h3 class="text-neutral-500">June 2023 - December 2025</h3>
	</div>
	<ul class="mx-4 list-outside list-disc overflow-auto">
		<li class="mb-2 text-neutral-400">
			> Developed a full-stack web application to monitor and retrieve data from data acquisition
			(DAQ) sites measuring VLF radio waves
		</li>
		<li class="mb-2 text-neutral-400">
			> Built a WebSocket API using AWS API Gateway, Lambda, and DynamoDB, enabling bidirectional
			communication between the website and 11 DAQ sites in under one second
		</li>
		<li class="mb-2 text-neutral-400">
			> Built a relational PostgreSQL database with multiple related tables supporting the website
			backend
		</li>
		<li class="text-neutral-400">
			> Built a responsive monitoring and data-retrieval frontend using Next.js and Tailwind CSS
		</li>
		<li class="text-neutral-400">
			> Developed an Node.js/Express.js REST API connecting the website, PostgreSQL database, and
			network-attached storage server (NAS), enabling users to view and download NAS files through
			the website
		</li>
		<li class="text-neutral-400">
			> Integrated the Python DAQ software with the Express.js REST API to auto upload generated
			files to NAS
		</li>
	</ul>
</article>
