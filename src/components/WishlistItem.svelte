<script>
	import Avatar from "./Avatar.svelte";

</script>
<style>
.container {
  border-bottom: 1px solid;
  border-bottom-color: rgba(180, 48, 242, 1);
  display: grid;
  padding: 5px 10px;
  grid-template:
    "avatar name"
    "avatar weapon"
  ;
}

.name {
  display: flex;
  justify-content: space-between;
}
</style>
<div class="container">
  <Avatar />
  <div class="name">
    <div>Raiden Shogun</div>
    <button>></button>
  </div>
  <div>
    The catch
  </div>
</div>
