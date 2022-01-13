<script>
  export let subLevel;
  export let price;
  export let users;
  export let storage;
  export let sendLimit;
  export let secondary = false;
  import Button from "./Button.svelte";
</script>

<div class="card" class:secondary>
  <h2>{subLevel}</h2>
  <ul>
    <li class="price"><span class="dollar">$</span>{price}</li>
    <li class="spec">{storage} Storage</li>
    <li class="spec">{users} Users Allowed</li>
    <li class="spec">Send up to {sendLimit} GB</li>
  </ul>
  <Button {secondary}>Learn more</Button>
</div>

<style>
  .card {
    --background: #fff;
    --text-color: var(--gray-blue);

    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    padding-top: 2rem;
    background: var(--background);
    border-radius: 10px;
    max-width: 350px;
    color: var(--text-color);
    padding-inline: 29px;
  }

  .card.secondary {
    --background: linear-gradient(135deg, #a2a7f0, #696edd);
    --text-color: #fff;
  }

  .dollar {
    font-size: 2.5rem;
    margin-right: 0.5rem;
  }

  .price {
    display: flex;
    font-size: 4.5rem;
    align-items: center;
    justify-content: center;
    border-top: none;
    color: var(--text-color);
  }

  ul {
    width: 100%;
    list-style: none;
    text-align: center;
  }

  li {
    text-decoration: none;
    border-top: 1px solid var(--text-color);
    padding-block: 13px;
  }

  li:last-child {
    border-bottom: 1px solid var(--text-color);
  }
</style>
