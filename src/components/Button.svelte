<script>
  export let secondary = false;
</script>

<button class:secondary><slot /></button>

<style>
  button {
    --background: linear-gradient(135deg, #a2a7f0, #696edd);
    --text-color: #fff;

    text-transform: uppercase;
    width: 100%;
    background: var(--background);
    color: var(--text-color);
    font-size: 0.8125rem;
    letter-spacing: 1.39px;
    padding-block: 0.875rem;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    margin-block: 2rem;
  }
<<<<<<< HEAD
  :global(.highlight button) {
    color: var(--highlight-btn);
    background: #fff;
=======

  button.secondary {
    --background: #fff;
    --text-color: #6d72de;
>>>>>>> c039f76 (Add unique style to highlighted card.)
  }
</style>
