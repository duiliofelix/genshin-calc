<script lang="ts">
    import { Modals, closeModal } from 'svelte-modals';
</script>

<style>
    .backdrop {
      position: fixed;
      top: 0;
      bottom: 0;
      right: 0;
      left: 0;
      background: rgba(0,0,0,0.50)
    }
</style>

<Modals>
    <div
        slot="backdrop"
        class="backdrop"
        on:click={closeModal}
    />
</Modals>

<slot></slot>