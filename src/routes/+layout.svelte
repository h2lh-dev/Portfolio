<script>
    import Header from "$lib/base/Header.svelte";
    import Footer from "$lib/base/Footer.svelte";
</script>

<Header />

<div class="slot"><slot/></div>

<Footer />


<style>
    .slot{
        min-height: calc(100vh - 180px);
    }
</style>