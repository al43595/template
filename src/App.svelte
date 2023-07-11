<script>
	export let name;
	import Voltage from "./Voltage.svelte";
	import Current from "./Current.svelte";

	let voltageInput = '';
	let currentInput = '';
</script>

<main>
	
	<h2> Gui Control</h2>
	<table>
		<thead>
			<tr>
				<th><strong>Voltage</strong></th>
				<th><strong>Current</strong></th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>
					<Voltage />
					<input bind:value={voltageInput} placeholder="Enter Voltage" />
					<button on:click={() => alert(
					`Voltage set to: ${voltageInput}`
					)}>Set Voltage</button>
				</td>
				<td>
					<Current />
					<input bind:value={currentInput} placeholder="Enter Current" />
					<button on:click={() => alert(`Current set to: ${currentInput}`)}>Set Current</button>
				</td>					
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

	input, button {
		margin: 0.5em;
	}

	button {
		background-color: #ff3e00;
		color: white;
		border: none;
		padding: 0.5em 1em;
		text-transform: uppercase;
		font-weight: bold;
		cursor: pointer;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>