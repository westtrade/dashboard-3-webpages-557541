<script lang="ts">
	export let title: string;
	export let data: string[][] = [];
</script>

<div class="card overflow-hidden">
	{#if title}
		<div class="card-header">
			<h4 class="card-title">{title}</h4>
		</div>
	{/if}

	<table class="table table table-bordered table-hover mb-0 border-transparent">
		<tbody>
			{#each data as cols}
				<tr>
					{#each cols as col, idx}
						{#if idx == 0}
							<th scope="row">{col}</th>
						{:else}
							<td>{col}</td>
						{/if}
						<!-- content here -->
					{/each}
				</tr>
			{/each}
		</tbody>
	</table>
</div>
