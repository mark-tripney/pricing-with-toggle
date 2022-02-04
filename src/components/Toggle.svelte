<script>
  export let monthly;
</script>

<div class="toggle-component">
  <p>Annual</p>
  <label class="toggle">
    <input type="checkbox" on:click />
    <span class="slider" />
  </label>
  <p>Monthly</p>
</div>

<style>
  .toggle-component {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1.5rem;
    margin-bottom: 5rem;
  }
  @media (min-width: 1050px) {
    .toggle-component {
      margin-bottom: 4rem;
    }
  }
  .toggle {
    position: relative;
    display: inline-block;
    width: 56px;
    height: 32px;
  }

  /* Hide default checkbox */
  .toggle input {
    opacity: 0;
    width: 0;
    height: 0;
  }

  .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: linear-gradient(135deg, #a2a7f0 0%, #696edd 100%);
    -webkit-transition: 0.2s;
    transition: 0.2s;
    border-radius: 16px;
  }

  .slider:before {
    position: absolute;
    content: "";
    height: 24px;
    width: 24px;
    right: 4px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: 0.2s;
    transition: 0.2s;
    border-radius: 50%;
  }

  input:checked + .slider {
    background-color: #2196f3;
  }

  input:focus + .slider {
    box-shadow: 0 0 1px #2196f3;
  }

  input:checked + .slider:before {
    transform: translateX(-24px);
  }

  .slider:hover {
    background: linear-gradient(135deg, #a2a7f0 0%, #696edd 100%);
    opacity: 0.5;
  }

  p {
    color: #6e728e;
    font-size: 0.9375rem;
    opacity: 0.5;
  }
</style>
