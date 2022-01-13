<script>
  export let subLevel;
  export let price;
  export let users;
  export let storage;
  export let sendLimit;
  export let highlight = false;
  import Button from "./Button.svelte";
</script>

<div class="card" class:highlight>
  <h2>{subLevel}</h2>
  <ul>
    <li class="price"><span class="dollar">$</span>{price}</li>
    <li class="spec">{storage} Storage</li>
    <li class="spec">{users} Users Allowed</li>
    <li class="spec">Send up to {sendLimit} GB</li>
  </ul>
  <Button {highlight}>Learn more</Button>
</div>

<style>
  .card {
    /* Variables for standard cards */
    --background: #fff;
    --text-colour: hsl(var(--gray-blue));
    --price-colour: var(--dark-gray-blue);
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    padding-top: 2rem;
    background: var(--background);
    border-radius: 10px;
    min-width: 327px;
    max-width: 327px;
    color: var(--text-colour);
    padding-inline: 29px;
    margin-bottom: 2rem;
  }
  @media (min-width: 1050px) {
    .card {
      min-width: 350px;
      max-width: 350px;
    }
    .card.highlight {
      height: 501px;
    }
  }

  .card.highlight {
    /* Variables for highlight card */
    --background: linear-gradient(135deg, #a2a7f0, #696edd);
    --text-colour: #fff;
    --price-colour: #fff;
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
    color: var(--price-colour);
  }

  ul {
    width: 100%;
    list-style: none;
    text-align: center;
  }

  li {
    text-decoration: none;
    /* TODO: Add some opacity to border */
    border-top: 1px solid var(--text-colour);
    padding-block: 13px;
  }

  li:last-child {
    /* TODO: Add some opacity to border */
    border-bottom: 1px solid var(--text-colour);
  }
</style>
