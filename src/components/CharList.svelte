<script lang="ts">
	import CharConfig from "../types/CharConfig";
    import CharListItem from "./CharListItem.svelte";
    import Container from "./Container.svelte";

    let list: CharConfig[] = [];

    const handleAddClick = () => {
        list.push(new CharConfig());

        // Trigger update
        list = list;
    };
</script>

<style>
    .container-header {
        background: linear-gradient(45deg, rgba(180, 48, 242, 1) 0%, rgba(139, 54, 247, 1) 100%);
        color: white;
        padding: 5px 10px;
    }
</style>

<Container>
    <div class="container-header">
        Lista
        <button on:click={handleAddClick}>+</button>
    </div>
    {#each list as item}
        <div>
            <CharListItem item={item}/>
        </div>
    {/each}
</Container>