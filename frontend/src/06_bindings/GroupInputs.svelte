<script>
  let scoops = 1;
  let flavours = ['Mint choc chip'];
  let menu = [
    'Cookies and cream',
    'Mint choc chip',
    'Raspberry ripple',
  ];

  function join(flavours) {
    if (flavours.length === 1) return flavours[0];
    return `${flavours.slice(0, -1).join(', ')} and ${flavours[flavours.length - 1]}`;
  }
</script>

<p><em>Size</em></p>

{#each [1, 2, 3] as value}
  <label>
    <input type=radio bind:group={scoops} name="scoops" {value}>
    {value} scoop{value > 1 ? 's' : ''}
  </label>
{/each}

<p><em>Flavours</em></p>

{#each menu as flavour}
	<label>
		<input type=checkbox bind:group={flavours} name="flavours" value={flavour}>
		{flavour}
	</label>
{/each}

<!--
  Note that a multi-select behaves exactly like a checkbox group as
  far as the binding is concerned :O
-->
<select multiple bind:value={flavours}>
	{#each menu as flavour}
		<option value={flavour}>
			{flavour}
		</option>
	{/each}
</select>

{#if flavours.length === 0}
	<p>Please select at least one flavour</p>
{:else if flavours.length > scoops}
	<p>Can't order more flavours than scoops!</p>
{:else}
	<p>
		You ordered {scoops} {scoops === 1 ? 'scoop' : 'scoops'}
		of {join(flavours)}
	</p>
{/if}
