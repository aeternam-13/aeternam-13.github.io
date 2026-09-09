<script lang="ts">
    let appName = "Salary calculator";
    let developerName = "aeternamdev";
    let contactEmail = "aeternamdev13@gmail.com";
    let lastUpdated = "September 2026";
</script>

<svelte:head>
    <title>MX Tax Calculator — aeternam</title>
</svelte:head>

<main class="container">
    <a href="/" class="back-link">← back to home</a>

    <h1>{appName}</h1>
    <p class="status">status: coming soon</p>
    <p class="description">
        Tax estimates for Mexican freelancers and small businesses under RESICO
        and Persona Física configurations.
    </p>

    <h1>Privacy Policy for {appName}</h1>
    <p><strong>Last updated:</strong> {lastUpdated}</p>

    <section>
        <h2>1. Data Collection and Usage</h2>
        <p class="description">
            {appName} does not collect, transmit, store, or share any personal data
            or user-entered information. All input values and calculations remain
            strictly in temporary local memory on your device and are discarded when
            you close the app.
        </p>
    </section>

    <section>
        <h2>2. Permissions</h2>
        <p class="description">
            This application requires no device permissions (such as Internet
            access, location, camera, or storage) to function.
        </p>
    </section>

    <section>
        <h2>3. Third-Party Services and Analytics</h2>
        <p class="description">
            This application does not use any third-party SDKs, analytics
            tracking, advertising networks, or external services.
        </p>
    </section>

    <section>
        <h2>4. Children's Privacy</h2>
        <p class="description">
            Because our application does not collect any personal information,
            it complies with privacy laws including COPPA (Children’s Online
            Privacy Protection Act) and GDPR.
        </p>
    </section>

    <section>
        <h2>5. Contact Us</h2>
        <p class="description">
            If you have any questions or suggestions regarding this Privacy
            Policy, please contact {developerName} at:
            <a href="mailto:{contactEmail}">{contactEmail}</a>
        </p>
    </section>
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
        line-height: 1.6;
    }
</style>
