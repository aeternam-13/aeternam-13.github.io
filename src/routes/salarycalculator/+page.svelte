<script lang="ts">
  let appName = "Salary calculator MX";
</script>

<svelte:head>
  <title>Salary calculator MX</title>
</svelte:head>

<main class="container">
  <a href="/" class="back-link">← back to home</a>

  <header>
    <h1>{appName}</h1>
    <p class="status">Salary decision tool for Mexican employees</p>
    <p class="description">
      Type your gross salary and benefits, get the <strong
        >real net you'd take home</strong
      >. Built for job hunting: when you get an offer at LinkedIn or a recruiter
      with a base salary and a list of "extras," type them in and see which
      offer is actually best — because a high base salary with no benefits often
      loses to a moderate one with good extras.
    </p>
  </header>

  <section>
    <h2>What is it?</h2>
    <p class="description">
      A fast, privacy-first salary calculator for people paid as <strong
        >salaried employees in Mexico</strong
      > under ISR and IMSS rules (LISR). Your numbers are calculated locally on your
      device.
    </p>
  </section>

  <section>
    <h2>What you enter</h2>
    <ul>
      <li>Gross salary and payment period (monthly / biweekly / annual)</li>
      <li>Aguinaldo — year-end bonus days</li>
      <li>Vacation days and vacation bonus (prima vacacional) %</li>
      <li>Savings fund (fondo de ahorro) toggle and %</li>
      <li>Grocery vouchers (vales de despensa) per month</li>
      <li>Annual extra bonus and gross PTU</li>
    </ul>
  </section>

  <section>
    <h2>What it calculates</h2>
    <ul>
      <li>
        ISR income tax and IMSS social-security deductions per statutory formula
      </li>
      <li>
        Base salary, aguinaldo, prima vacacional, savings fund, PTU, and annual
        bonus split into gross / tax / net
      </li>
      <li>Totals broken down into annual, monthly, and biweekly views</li>
      <li>
        Gross, tax, and net breakdown charts, so you can see where every peso
        goes
      </li>
    </ul>
  </section>

  <section>
    <h2>Also baked in</h2>
    <ul>
      <li>A Guide screen that explains each benefit term, plus a Glossary</li>
      <li>
        Bilingual English / Español, with light, dark, and high-contrast themes
      </li>
      <li>Privacy-first: typed values never leave your device</li>
    </ul>
  </section>

  <p class="description"><strong>Free</strong>, supported by ads.</p>

  <footer>
    <a href="/salarycalculator/privacy" class="nav-link">Privacy Policy</a>
  </footer>
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
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 500;
    margin: 0 0 0.5rem;
  }

  h2 {
    font-size: 1.35rem;
    margin-top: 1.5rem;
  }

  .status {
    font-family: "JetBrains Mono", monospace;
    font-size: 0.85rem;
    color: var(--ink-soft, #475569);
    margin-bottom: 1.5rem;
  }

  .description {
    font-size: 1.05rem;
    line-height: 1.6;
  }

  ul {
    line-height: 1.6;
  }

  footer {
    margin-top: 3rem;
    padding-top: 1.5rem;
    border-top: 1px solid var(--ink-soft, #cbd5e1);
  }

  .nav-link {
    color: var(--patina, #2563eb);
    font-family: "JetBrains Mono", monospace;
    font-size: 0.9rem;
    text-decoration: none;
  }

  .nav-link:hover {
    text-decoration: underline;
  }
</style>
