<script>
  export let items = []
  export let activeTab = 1

  const handleClick = tabValue => () => (activeTab = tabValue);
</script>

<ul>
  {#each items as item}
    <li class={activeTab === item.value ? "active" : ""}>
      <button on:click={handleClick(item.value)}>{item.label}</button>
    </li>
  {/each}
</ul>
{#each items as item}
  {#if activeTab === item.value}
  <div class="tab">
    <svelte:component this={item.component} {...item.props} />
  </div>
  {/if}
{/each}

<style>
    .tab {
    margin-top: 20px;
  }

  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding-left: 0;
    margin-bottom: 0;
    list-style: none;
    margin-bottom: 2.5rem;
  }

  li {
    margin: 6px 6px;
		margin-bottom: -1px;
	}

  li.active > button {
    background-color: var(--secondary);
  }

  button {
    border: 1px solid transparent;
    background-color: transparent;
    color: #fff;
    text-transform: uppercase;
    border-radius: 0.25rem;
    display: block;
    padding: .8rem 1.2rem;
    cursor: pointer;
    border: none;
    transition: background 250ms ease-out;
  }

  button:hover {
    border-color: #e9ecef #e9ecef #dee2e6;
  }
</style>