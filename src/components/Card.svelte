<script>
  export let subLevel;
  export let price;
  export let users;
  export let storage;
  export let sendLimit;
  import Button from './Button.svelte';
</script>

<div class="card">
  <h2>{subLevel}</h2>
  <ul>
    <li class="price"><span class="dollar">$</span>{price}</li>
    <li class="spec">{storage} Storage</li>
    <li class="spec">{users} Users Allowed</li>
    <li class="spec">Send up to {sendLimit} GB</li>
  </ul>
  <Button>Learn more</Button>
</div>

<style>
  .card {
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    padding-top: 2rem;
    background-color: #fff;
    border-radius: 10px;
    max-width: 350px;
    color: var(--gray-blue);
    padding-inline: 29px;
    margin-bottom: 2rem;
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
    color: var(--dark-gray-blue);
  }
  :global(.highlight .price) {
    color: #fff;
  }
  ul {
    width: 100%;
    list-style: none;
    text-align: center;
  }
  li {
    text-decoration: none;
    border-top: 1px solid hsla(var(--gray-blue) / 0.4);
    padding-block: 13px;
  }
  :global(.highlight li) {
    border-top: 1px solid hsla(var(--white) / 0.5);
  }
  li:last-child {
    border-bottom: 1px solid hsla(var(--gray-blue) / 0.4);
  }
  :global(.highlight li:last-child) {
    border-bottom: 1px solid hsla(var(--white) / 0.5);
  }
</style>
