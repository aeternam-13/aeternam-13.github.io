<script lang="ts">
</script>

<svelte:head>
    <title>MX Tax Calculator — aeternam</title>
</svelte:head>

<main class="container">
    <a href="/" class="back-link">← back to home</a>

    <h1>mx tax calculator</h1>
    <p class="status">status: coming soon</p>
    <p class="description">
        Tax estimates for Mexican freelancers and small businesses under RESICO
        and Persona Física configurations.
    </p>
</main>

<style>
    .container {
        min-height: 100vh;
        padding: 2.5rem clamp(1.5rem, 5vw, 5rem);
        background: var(--stone, #f0f4f8);
        color: var(--ink, #0f172a);
        font-family: "Fraunces", Georgia, serif;
    }

    .back-link {
        display: inline-block;
        color: var(--patina, #2563eb);
        text-decoration: none;
        font-family: "JetBrains Mono", monospace;
        font-size: 0.9rem;
        margin-bottom: 2rem;
    }

    .back-link:hover {
        text-decoration: underline;
    }

    h1 {
        font-size: clamp(2rem, 5vw, 3.5rem);
        font-weight: 500;
        margin: 0 0 0.5rem;
    }

    .status {
        font-family: "JetBrains Mono", monospace;
        font-size: 0.85rem;
        color: var(--ink-soft, #475569);
        margin-bottom: 1.5rem;
    }

    .description {
        font-size: 1.1rem;
        max-width: 40ch;
        line-height: 1.6;
    }
</style>
