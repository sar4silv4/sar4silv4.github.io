<script>
	export let title = 'Y';
</script>

<link
	rel="stylesheet"
	href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
/>

<div class="d-flex flex-column min-vh-100">
	<header class="bg-primary text-white py-3">
		<div class="container text-center">
			<h1>{title}</h1>
		</div>
	</header>

	<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
		<div class="container">

			<!-- svelte-ignore a11y_consider_explicit_label -->
			<button
				class="navbar-toggler"
				type="button"
				data-bs-toggle="collapse"
				data-bs-target="#navbarNav"
			>
				<span class="navbar-toggler-icon"></span>
			</button>
			<div class="collapse navbar-collapse" id="navbarNav">
				<ul class="navbar-nav">
					<li class="nav-item">
						<a class="nav-link" href="/mensagens">Mensagens</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" href="/calls">Chamadas perdidas</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" href="/status">Status</a>
					</li>
				</ul>
			</div>
		</div>
	</nav>

	<main class="container my-4">
		<slot />
	</main>

	<footer class="bg-dark text-white text-center py-3 mt-auto">
		<p>&copy; {new Date().getFullYear()} y.com Todos os direitos reservados.</p>
	</footer>
</div>
