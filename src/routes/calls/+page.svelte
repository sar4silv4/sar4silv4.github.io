<script>
	let chamadas = $state ([
		{ id: 1, tipo: 'perdida', numero: 'Mãe', horario: 'Hoje ás 10:30' },
		{ id: 2, tipo: 'perdida', numero: 'Mãe', horario: 'Hoje ás 10:27' },
		{ id: 3, tipo: 'perdida', numero: 'Mãe', horario: 'Hoje ás 10:24' },
		{ id: 4, tipo: 'perdida', numero: 'Mãe', horario: 'Hoje ás 10:21' },
		{ id: 5, tipo: 'perdida', numero: 'Mãe', horario: 'Hoje ás 10:18' },
		{ id: 6, tipo: 'recebida', numero: 'Pai', horario: 'Ontem ás 16:39' },
		{ id: 7, tipo: 'efetuada', numero: 'Ana Júlia', horario: 'Ontem ás 08:54' }
	]);

	let selecionadas = $state([]);

	function excluirselecionadas() {
		for (const selecionada of selecionadas) {
			const i = chamadas.indexOf (selecionada)
			chamadas.splice(i, 1)
		}
	}

	function getBackground(tipo) {
		return tipo === 'perdida'
			? 'bg-danger-subtle'
			: tipo === 'recebida'
				? 'bg-success-subtle'
				: 'bg-primary-subtle';
	}
</script>

<h2>Histórico de Chamadas</h2>

<div class="list-group">
	{#each chamadas as chamada (chamada.id)}
	<label>
		<div
			class="list-group-item d-flex justify-content-between align-items-center {getBackground(
				chamada.tipo
			)}"
		>
			<div>
				<input
					type="checkbox"
					value={chamada}
					bind:group={selecionadas}
					/>
				<strong>{chamada.tipo.charAt(0).toUpperCase() + chamada.tipo.slice(1)}</strong> - {chamada.numero}
				({chamada.horario})
			</div>
		</div></label>
	{/each}
</div>
<div class="d-grid gap-2 d-md-flex justify-content-md-end">
	<button type="button" class="btn btn-danger" onclick="{excluirselecionadas}">excluir selecionadas</button>
</div>

<style>
	.list-group-item {
		padding: 10px;
		border-radius: 5px;
		margin-bottom: 5px;
	}

	.btn {
		margin-bottom: 10px;
	}
</style>
