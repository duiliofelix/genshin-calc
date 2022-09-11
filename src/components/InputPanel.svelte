<script lang="ts">
import LevelForm from "./LevelForm.svelte";
import WeaponForm from "./WeaponForm.svelte";

let panel = 0;

const config = {
  charLvl: '1',
  weapon: {
    name: '',
    level: '1',
  },
};

const handleLevelSelection = (event: any) => {
  config.charLvl = event.target.value;
};

const handleWeaponSelection = (event: any) => {
  config.weapon = event.detail;
  console.log(config);
};
</script>

<div class="container">
  <nav>
    <button on:click={() => panel = 0}>Level</button>
    <button on:click={() => panel = 1}>Arma</button>
    <button on:click={() => panel = 2}>Artefatos</button>
    <button on:click={() => panel = 3}>Constelação</button>
    <button on:click={() => panel = 4}>Talento</button>
  </nav>
  <div class="content">
    {#if panel === 1}
      <WeaponForm on:change={handleWeaponSelection} />
    {:else}
      <LevelForm on:change={handleLevelSelection} />
    {/if}
  </div>
</div>

<style>
.container {
  border: 1px solid black;
  border-radius: 5px 0 0 5px;
}

.content {
  padding: 10px;
}

nav {
  display: flex;
}

nav > button {
  background-color: initial;
  border: none;
  border-bottom: thin solid black;
}

</style>