<script>
	import WishlistItem from "../components/WishlistItem.svelte";
</script>

<svelte:head>
    <style>
        body {
            background: linear-gradient(160deg, rgba(35, 26, 57, 1) 40%, rgba(23, 2, 106, 1) 100%);
            color: white;
            min-height: 100vh;
        }
    </style>
</svelte:head>

<style>
    .container {
        background-color: rgba(19, 26, 29, .7);
        border-radius: 2px;
        overflow: hidden;
    }

    .container-header {
        background: linear-gradient(45deg, rgba(180, 48, 242, 1) 0%, rgba(139, 54, 247, 1) 100%);
        color: white;
        padding: 5px 10px;
    }

    .grid {
        display: grid;
        grid-template:
         "header header"
         "list main"
         / 300px 2fr
        ;
        gap: 10px;
    }

    .header {
        grid-area: header;
    }
</style>

<div class="grid">
    <div class="container header">
        <span>Wishlist</span>
        <span>Calculator</span>
    </div>
    <div class="container">
        <div class="container-header">
            Lista
            <button>+</button>
        </div>
        <WishlistItem />
        <WishlistItem />
        <WishlistItem />
    </div>
    <div class="container">
        teste
    </div>
</div>
