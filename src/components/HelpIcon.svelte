<script>
  import HoverTooltip from "./HoverTooltip.svelte";

  let { children } = $props();
</script>

<div class="container">
  <HoverTooltip>
    {#snippet tooltip()}
      {@render children?.()}
    {/snippet}
    <div class="icon fas fa-question-circle"></div>
  </HoverTooltip>
</div>

<style lang="scss">
  .container {
    position: relative;
  }

  .icon {
    font-size: 0.9rem;
    padding: 2px;

    color: var(--color-text-soft);

    &:hover {
      color: var(--color-text);
    }
  }
</style>
