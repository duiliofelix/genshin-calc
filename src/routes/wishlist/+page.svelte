<script>
    import CharList from "../../components/organisms/CharList.svelte";
    import Container from "../../components/atoms/Container.svelte";
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
    <CharList />
    <Container>
        teste
    </Container>
</div>
