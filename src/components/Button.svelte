<script>
  export let highlight = false;
</script>

<button class:highlight><slot /></button>

<style>
  button {
    --background: linear-gradient(135deg, #a2a7f0, #696edd);
    --text-colour: #fff;

    text-transform: uppercase;
    width: 100%;
    background: var(--background);
    color: var(--text-colour);
    font-size: 0.8125rem;
    letter-spacing: 1.39px;
    padding-block: 0.875rem;
    border: 1px solid transparent;
    border-radius: 6px;
    cursor: pointer;
    margin-block: 2rem;
  }
  button.highlight {
    --background: #fff;
    --text-colour: #6d72de;
  }
  button:hover {
    background: #fff;
    color: #6d72de;
    border: 1px solid #6d72de;
  }
  button.highlight:hover {
    border: 1px solid #fff;
    color: #fff;
    background: none;
  }
</style>
