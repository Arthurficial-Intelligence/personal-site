<script>
    import Nav from "../components/Nav.svelte";
</script>

<div>
    <Nav />
    <slot />
</div>

<style>
    div {
        display: flex;
        justify-content: flex-start;
        width: 100%;
    }
</style>
