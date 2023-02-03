<script lang="ts">
	import type CharConfig from "../types/CharConfig";

    export let item: CharConfig;
</script>

<style>
    .list-item {
        border-bottom: 1px solid;
        border-bottom-color: rgba(180, 48, 242, 1);
        padding: 5px 10px;
    }
</style>

<div class="list-item">
    <div>img</div>
    <div>
        <div>
            <div>{item.name || ''}</div>
            <button>></button>
        </div>
        <div>
            The catch
        </div>
    </div>
</div>