<script>
  export let subLevel;
  export let price;
  export let users;
  export let storage;
  export let sendLimit;
</script>

<div class="card">
  <h2>{subLevel}</h2>
  <ul>
    <li class="price"><span class="dollar">$</span>{price}</li>
    <li class="spec">{storage} GB Storage</li>
    <li class="spec">{users} Users Allowed</li>
    <li class="spec">Send up to {sendLimit} GB</li>
  </ul>
  <button>Learn more</button>
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
  ul {
    width: 100%;
    list-style: none;
    text-align: center;
  }
  li {
    text-decoration: none;
    border-top: 1px solid var(--gray-blue);
    padding-block: 13px;
  }
  li:last-child {
    border-bottom: 1px solid var(--gray-blue);
  }
  button {
    text-transform: uppercase;
    width: 100%;
    background: linear-gradient(#a2a7f0, #696edd);
    color: #fff;
    font-size: 0.8125rem;
    letter-spacing: 1.39px;
    padding-block: 0.875rem;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    margin-block: 2rem;
  }
</style>
