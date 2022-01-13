<script>
  export let monthly;
</script>

<button on:click>{monthly ? 'Annual' : 'Monthly'}</button>

<style>
  button {
    border: none;
    color: white;
    background-color: coral;
    padding: 1rem 1.5rem;
    cursor: pointer;
    border-radius: 10px;
    margin-bottom: 4rem;
  }
  button:hover {
    background: palevioletred;
  }
</style>
