<script>
    import Header from "$lib/base/Header.svelte";
    import Footer from "$lib/base/Footer.svelte";
</script>

<Header />

<main class="main-content"><slot/></main>

<Footer />


<style>
    :global(*) {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    :global(body) {
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
        background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
        color: #e2e8f0;
        line-height: 1.6;
    }

    :global(html) {
        scroll-behavior: smooth;
    }

    .main-content {
        min-height: calc(100vh - 120px);
        padding: 60px 20px;
        max-width: 1400px;
        margin: 0 auto;
    }

    :global(h1, h2, h3, h4, h5, h6) {
        font-weight: 700;
        letter-spacing: -0.5px;
    }

    :global(a) {
        color: #60a5fa;
        text-decoration: none;
        transition: color 0.3s ease;
    }

    :global(a:hover) {
        color: #93c5fd;
    }
</style>