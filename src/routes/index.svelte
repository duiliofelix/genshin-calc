<script lang="ts">
import InputPanel from "../components/InputPanel.svelte";
import CharPicker from "../components/CharPicker.svelte";
import Stats from "../components/Stats.svelte";
import Results from "../components/Results.svelte";

let charLevel = '1';
const handleInputChange = (e) => {
  charLevel = e.detail.charLvl;
}
</script>

<CharPicker />
<div class="content">
  <InputPanel on:change={handleInputChange} />
  <Stats level={charLevel} />
  <Results baseAtk={234} baseWpnAtk={510} />
</div>

<style>
.content {
  display: flex;
  padding: 10px 0;
}
</style>
