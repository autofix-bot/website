<script>
  import Section from "../section.svelte";

  export let otherPlans;
</script>

<style lang="scss">
  h1 {
    text-align: center;
    text-transform: capitalize;
  }

  .plan {
    display: flex;
    padding: var(--small) var(--xx-small) var(--small);
    border-bottom: 1px solid var(--divider);

    @media (max-width: 768px) {
      flex-direction: column;
    }

    &__header {
      flex: 0 0 35%;
    }

    &__body {
      flex: 1;

      & :global(strong) {
        color: var(--black);
      }
    }
  }

  p:not(:last-of-type) {
    margin-bottom: var(--xx-small);
  }

  .btn-cta {
    margin-top: var(--small);
  }
</style>

<Section>
  <h1>Open source, self hosting, and students</h1>
  <div class="plans">
    {#each otherPlans as p}
      <div class="plan divider">
        <div class="plan__header">
          <h3 class="h4">{p.title}</h3>
        </div>
        <div class="plan__body">
          {#each p.paragraphs as para}
            <p>{@html para}</p>
          {/each}
          <a href={p.btnHref} class="btn-cta">{p.btnText}</a>
        </div>
      </div>
    {/each}
  </div>
</Section>
