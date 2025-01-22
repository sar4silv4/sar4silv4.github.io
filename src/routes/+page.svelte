<script>
	export let title = 'Catálogo de Produtos';
</script>

<link
	rel="stylesheet"
	href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css"
/>

<div class="d-flex flex-column min-vh-100">
	<header class="bg-dark text-white py-3">
		<div class="container">
			<h1 class="text-center">{title}</h1>
		</div>
	</header>

	<nav class="navbar navbar-expand-lg navbar-light bg-light">
		<div class="container">
			<a class="navbar-brand" href="/">Loja Online</a>
			<div class="collapse navbar-collapse" id="navbarNav">
				<ul class="navbar-nav">
					<li class="nav-item">
						<a class="nav-link" href="/produtos">Produtos</a>
					</li>
					<li class="nav-item">
						<a class="nav-link" href="/about">Sobre</a>
					</li>
				</ul>
			</div>
		</div>
	</nav>

	<main class="container my-4">
		<slot />
	</main>

	<footer class="bg-dark text-white text-center py-3 mt-auto">
		<div class="container">
			<p>&copy; {new Date().getFullYear()} Todos os direitos reservados.</p>
		</div>
	</footer>
</div>
