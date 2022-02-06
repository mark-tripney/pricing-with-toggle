<div class="toggle-component">
  <input class="input" id="toggle" type="checkbox" on:click />
  <label class="label" for="toggle">
    <span class="option annual">Annual</span>
    <span class="switch">
      <span class="slider" />
    </span>
    <span class="option monthly">Monthly</span>
  </label>
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

  .label {
    pointer-events: none;
    display: flex;
    align-items: center;
    gap: 1.5rem;
  }

  .switch,
  .input:checked + .label .monthly,
  .input:not(:checked) + .label .annual {
    pointer-events: all;
    cursor: pointer;
  }

  .option:not(:checked):hover {
    opacity: 1;
  }

  .input {
    display: none;
  }

  .switch {
    position: relative;
    display: inline-block;
    width: 56px;
    height: 32px;
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
  }

  .slider:before {
    position: absolute;
    content: "";
    height: 24px;
    width: 24px;
    left: 28px;
    bottom: 4px;
    background-color: white;
    -webkit-transition: 0.2s;
    transition: 0.2s;
  }

  input:checked + .label .slider {
    background-color: #2196f3;
  }

  input:focus + .label .slider {
    box-shadow: 0 0 1px #2196f3;
  }

  input:checked + .label .slider:before {
    transform: translateX(-24px);
  }

  .slider {
    border-radius: 34px;
  }

  .slider:before {
    border-radius: 50%;
  }

  .slider:hover {
    background: linear-gradient(135deg, #a2a7f0 0%, #696edd 100%);
    opacity: 0.5;
  }

  .annual,
  .monthly {
    color: #6e728e;
    font-size: 0.9375rem;
    opacity: 0.5;
  }
</style>
