<script lang="ts">
    const github = "https://github.com/aeternam-13";
    const email = "macg.ae1313@gmail.com";

    const stack: string[] = ["flutter", "kotlin", "swift", "go"];

    type App = {
        name: string;
        description: string;
        href: string;
        status: "live" | "soon";
    };

    const apps: App[] = [
        {
            name: "mx tax calculator",
            description:
                "tax estimates for Mexican freelancers and small businesses.",
            href: "/mxtaxcalculator",
            status: "soon",
        },
    ];
</script>

<svelte:head>
    <title>aeternam — Lead Software Developer</title>
</svelte:head>

<main class="page">
    <header class="nav">
        <span class="mark">ae.</span>
        <div class="nav-links">
            <a class="nav-link" href={github}>github</a>
            <a class="nav-link" href={`mailto:${email}`}>say hello</a>
        </div>
    </header>

    <section class="hero">
        <div class="hero-copy">
            <h1>aeternam</h1>
            <p class="role">
                Lead Software Developer — Flutter, Go, Kotlin, Swift. Android, iOS &amp; Backend.
            </p>
            <p class="lede">
                I've spent the last several years building payment and POS
                software used by millions of people daily. Now shipping my own
                apps, starting here — and picking up Go as I move into backend
                work.
            </p>
        </div>

        <div class="terminal">
            <div class="terminal-bar">
                <span class="dot"></span>
                <span class="dot"></span>
                <span class="dot"></span>
            </div>
            <pre class="terminal-body"><span class="prompt">$</span> whoami
Marco Antonio Castro Gutiérrez
aeternam — mobile developer

<span class="prompt">$</span> cat stack.txt
Flutter · Kotlin · Swift · Go (learning)<span class="cursor">▌</span></pre>
        </div>
    </section>

    <section class="apps">
        {#each apps as app}
            <a class="app-card" href={app.href}>
                <span class="app-name">{app.name}</span>
                <span class="app-status" class:soon={app.status === "soon"}>
                    {app.status === "live" ? "on the store" : "coming soon"}
                </span>
                <p class="app-desc">{app.description}</p>
            </a>
        {/each}
    </section>

    <footer class="stack">
        {#each stack as tool, i}
            <span class="tool" class:first={i === 0}>{tool}</span>
        {/each}
    </footer>
</main>

<style>
    :global(:root) {
        --stone: #f0f4f8; /* Soft light ice-blue base background */
        --ink: #0f172a; /* Deep slate/navy for primary text */
        --ink-soft: #475569; /* Slate blue for secondary text */
        --patina: #2563eb; /* Vibrant primary accent blue */
        --patina-light: #60a5fa; /* Light accent blue for terminal prompt */
        --line: #cbd5e1; /* Subtle cool border divider */
        --terminal-bg: #0f172a; /* Dark navy for terminal background */
        --terminal-text: #f1f5f9; /* Bright text inside terminal */
    }
    :global(html, body) {
        margin: 0;
        padding: 0;
        background: var(--stone);
        color: var(--ink);
    }

    :global(*) {
        box-sizing: border-box;
    }

    .page {
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        padding: 2.5rem clamp(1.5rem, 5vw, 5rem);
        font-family: "Fraunces", Georgia, serif;
    }

    .nav {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-bottom: 2rem;
        border-bottom: 1px solid var(--line);
    }

    .mark {
        font-size: 1.1rem;
        letter-spacing: 0.02em;
    }

    .nav-links {
        display: flex;
        gap: 1.5rem;
    }

    .nav-link {
        color: var(--ink);
        text-decoration: none;
        font-size: 0.95rem;
        border-bottom: 1px solid var(--patina);
        padding-bottom: 0.15rem;
    }

    .nav-link:hover,
    .nav-link:focus-visible {
        color: var(--patina);
    }

    .nav-link:focus-visible {
        outline: 2px solid var(--patina);
        outline-offset: 4px;
    }

    .hero {
        flex: 1;
        display: grid;
        grid-template-columns: minmax(0, 1.1fr) minmax(0, 0.9fr);
        gap: clamp(2rem, 5vw, 5rem);
        align-items: center;
        padding: clamp(3rem, 8vh, 6rem) 0;
    }

    .hero-copy {
        max-width: 40rem;
    }

    .hero-copy h1 {
        font-size: clamp(3rem, 8vw, 5.5rem);
        font-weight: 500;
        line-height: 0.95;
        margin: 0 0 1.25rem;
        letter-spacing: -0.01em;
    }

    .role {
        font-size: 1.15rem;
        color: var(--ink-soft);
        margin: 0 0 1.5rem;
    }

    .lede {
        font-size: 1.05rem;
        line-height: 1.65;
        color: var(--ink);
        max-width: 32ch;
    }

    .lede em {
        font-style: italic;
        color: var(--patina);
    }

    .terminal {
        background: var(--terminal-bg);
        border-radius: 6px;
        overflow: hidden;
        box-shadow: 0 1px 0 rgba(0, 0, 0, 0.25);
        justify-self: stretch;
    }

    .terminal-bar {
        display: flex;
        gap: 0.4rem;
        padding: 0.7rem 0.9rem;
        border-bottom: 1px solid rgba(219, 213, 199, 0.12);
    }

    .dot {
        width: 8px;
        height: 8px;
        border-radius: 50%;
        background: rgba(219, 213, 199, 0.25);
    }

    .terminal-body {
        margin: 0;
        padding: 1.5rem 1.25rem 1.75rem;
        font-family: "JetBrains Mono", "Courier New", monospace;
        font-size: 0.9rem;
        line-height: 1.8;
        color: var(--terminal-text);
        white-space: pre-wrap;
    }

    .prompt {
        color: var(--patina-light);
    }

    .cursor {
        animation: blink 1.1s steps(1) infinite;
    }

    @media (prefers-reduced-motion: reduce) {
        .cursor {
            animation: none;
        }
    }

    @keyframes blink {
        0%,
        49% {
            opacity: 1;
        }
        50%,
        100% {
            opacity: 0;
        }
    }

    .apps {
        display: flex;
        flex-wrap: wrap;
        gap: 1rem;
        padding: 0 0 2rem;
    }

    .app-card {
        display: block;
        padding: 1rem 1.25rem;
        border: 1px solid var(--line);
        border-radius: 6px;
        text-decoration: none;
        color: var(--ink);
        min-width: 14rem;
    }

    .app-card:hover,
    .app-card:focus-visible {
        border-color: var(--patina);
    }

    .app-card:focus-visible {
        outline: 2px solid var(--patina);
        outline-offset: 2px;
    }

    .app-name {
        font-family: "JetBrains Mono", monospace;
        font-size: 0.9rem;
    }

    .app-status {
        font-family: "JetBrains Mono", monospace;
        font-size: 0.75rem;
        color: var(--patina);
        margin-left: 0.5rem;
    }

    .app-status.soon {
        color: var(--ink-soft);
    }

    .app-desc {
        margin: 0.5rem 0 0;
        font-family: "Fraunces", serif;
        font-size: 0.95rem;
        color: var(--ink-soft);
    }

    .stack {
        display: flex;
        flex-wrap: wrap;
        gap: 0.9rem;
        padding-top: 1.5rem;
        border-top: 1px solid var(--line);
        font-family: "JetBrains Mono", "Courier New", monospace;
        font-size: 0.85rem;
        color: var(--ink-soft);
    }

    .tool {
        padding-left: 0.9rem;
        border-left: 1px solid var(--line);
    }

    .tool.first {
        padding-left: 0;
        border-left: none;
    }

    @media (max-width: 760px) {
        .hero {
            grid-template-columns: 1fr;
        }
    }
</style>
