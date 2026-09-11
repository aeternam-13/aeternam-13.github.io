<script lang="ts">
    let appName = "Salary calculator";
    let developerName = "aeternamdev";
    let contactEmail = "aeternamdev13@gmail.com";
    let lastUpdated = "September 2026";
</script>

<svelte:head>
    <title>Privacy Policy — {appName}</title>
</svelte:head>

<main class="container">
    <a href="/salarycalculatormx" class="back-link">← back to Salary calculator</a>

    <h1>Privacy Policy for {appName}</h1>
    <p class="status"><strong>Last updated:</strong> {lastUpdated}</p>

    <section>
        <h2>1. Data Collection and Usage</h2>
        <p class="description">
            {appName} does not collect, transmit, store, or share any personal salary
            information, tax estimations, or user-entered numbers. All calculation
            inputs remain strictly in temporary local memory on your device and are
            cleared when the app is closed.
        </p>
    </section>

    <section>
        <h2>2. Network & Permissions</h2>
        <p class="description">
            This application requires network access solely to retrieve
            advertisements delivered by third-party ad networks. No permissions
            are requested or required to access sensitive local device data
            (such as contacts, camera, or location).
        </p>
    </section>

    <section>
        <h2>3. Third-Party Advertising (Google AdMob)</h2>
        <p class="description">
            This app uses <strong>Google AdMob</strong> to display advertisements.
            AdMob may collect and process device identifiers, IP addresses, and general
            network diagnostic data to serve localized or personalized ads.
        </p>
        <p class="description">
            To learn more about how Google AdMob collects and uses data, refer
            to
            <a
                href="https://policies.google.com/technologies/ads"
                target="_blank"
                rel="noopener noreferrer"
                >Google’s Advertising & Privacy Policies</a
            >.
        </p>
    </section>

    <section>
        <h2>4. Children's Privacy</h2>
        <p class="description">
            This application does not knowingly collect or solicit personal data
            from children under the age of 13, in compliance with COPPA and GDPR
            frameworks.
        </p>
    </section>

    <section>
        <h2>5. Contact Information</h2>
        <p class="description">
            If you have questions or suggestions regarding this Privacy Policy,
            please contact {developerName} at:
            <a href="mailto:{contactEmail}">{contactEmail}</a>.
        </p>
    </section>
</main>

<style>
    .container {
        min-height: 100vh;
        padding: 2.5rem clamp(1.5rem, 5vw, 5rem);
        background: transparent;
        color: var(--ink, #0f172a);
        font-family: "Fraunces", Georgia, serif;
        max-width: 800px;
        margin: 0 auto;
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
        font-size: clamp(1.8rem, 4vw, 2.5rem);
        font-weight: 500;
        margin: 0 0 0.5rem;
    }

    h2 {
        font-size: 1.25rem;
        margin-top: 1.5rem;
    }

    .status {
        font-family: "JetBrains Mono", monospace;
        font-size: 0.85rem;
        color: var(--ink-soft, #475569);
        margin-bottom: 2rem;
    }

    .description {
        font-size: 1.05rem;
        line-height: 1.6;
    }

    a {
        color: var(--patina, #2563eb);
    }
</style>
