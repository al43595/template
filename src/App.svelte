<script>
	export let name;
	import Voltage from "./Voltage.svelte";
	import Current from "./Current.svelte";

	let voltageInput = '';
	let currentInput = '';
</script>

<main>
	<div class="hv-buttons">
		<button class="hv-button hv-on">HVON</button>
		<button class="hv-button hv-off">HV OFF</button>
	</div>
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
					<button on:click={() => alert(
						`Current set to: ${currentInput}`
						)}>Set Current</button>
				</td>					
			</tr>
		</tbody>
	</table>
	<h2> Gui Control</h2>
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

	th, input, button{
		text-align: left;
		padding: 0.5em;
	}

	
	.hv-button {
		margin: 0.5em;
		border: none;
		padding: 0.5em 1em;
		text-transform: uppercase;
		font-weight: bold;
		cursor: pointer;
		width: auto;
	}

	.hv-on {
		background-color: red;
		color: white;
	}

	.hv-off {
		background-color: green;
		color: white;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>