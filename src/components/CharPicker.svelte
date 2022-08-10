<script lang="ts">
import CharButton from "./CharButton.svelte";
</script>

<div class="container">
  <CharButton>char 1</CharButton>
  <CharButton>char 2</CharButton>
  <CharButton>char 3</CharButton>
  <CharButton>char 4</CharButton>
  <CharButton>char 5</CharButton>
</div>

<style>
.container {
  box-shadow: 0px 2px 1px rgba(0,0,0,.65);
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 10px;
}
</style>
