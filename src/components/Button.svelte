<script>
</script>

<button><slot /></button>

<style>
  button {
    text-transform: uppercase;
    width: 100%;
    background: linear-gradient(135deg, #a2a7f0, #696edd);
    color: #fff;
    font-size: 0.8125rem;
    letter-spacing: 1.39px;
    padding-block: 0.875rem;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    margin-block: 2rem;
  }
  :global(.highlight button) {
    color: var(--highlight-btn);
    background: hsl(var(--white));
  }
</style>
