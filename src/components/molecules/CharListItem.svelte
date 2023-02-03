<script lang="ts">
	import { createEventDispatcher } from "svelte";
	import type CharConfig from "../../types/CharConfig";
	import Avatar from "../atoms/Avatar.svelte";

    export let item: CharConfig;

    const dispatch = createEventDispatcher();

    const handleEditClick = () => dispatch('edit');
</script>

<style>
    .list-item {
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

<div class="list-item">
    <Avatar />
    <div>
        <div class="name">
            <div>{item.name || ''}</div>
            <button on:click={handleEditClick}>
                >
            </button>
        </div>
        <div>
            The catch
        </div>
    </div>
</div>