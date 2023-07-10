<script>
	export let name;
	import Voltage from "./Voltage.svelte";
	import Current from "./Current.svelte";
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<h2> Gui start</h2>
	<table>
		<thead>
			<tr>
				<th><strong>Voltage</strong></th>
				<th><strong>Current</strong></th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td><Voltage /></td>
				<td><Current /></td>
			</tr>
		</tbody>
	</table>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	h2 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	table{
		width: 100%;
		margin-top: 1em;
	}

	th {
		text-align: left;
		padding: 0.5em;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>