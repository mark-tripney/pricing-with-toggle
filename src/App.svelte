<script>
  import Card from "./components/Card.svelte";
  import Footer from "./components/Footer.svelte";
  import Toggle from "./components/Toggle.svelte";
  let monthly = true;

  // Card details
  const basicMonthly = {
    subLevel: "Basic",
    price: 19.99,
    storage: "500 GB",
    users: 2,
    sendLimit: 3,
  };
  const proMonthly = {
    subLevel: "Professional",
    price: 24.99,
    storage: "1 TB",
    users: 5,
    sendLimit: 10,
  };
  const masterMonthly = {
    subLevel: "Master",
    price: 39.99,
    storage: "2 TB",
    users: 10,
    sendLimit: 20,
  };

  const handleClick = () => {
    monthly = !monthly;
    if (monthly) {
      basicMonthly.price = 19.99;
      proMonthly.price = 24.99;
      masterMonthly.price = 39.99;
    } else {
      basicMonthly.price = 199.99;
      proMonthly.price = 249.99;
      masterMonthly.price = 399.99;
    }
  };
</script>

<div class="content-wrapper">
  <header>
    <h1>Our Pricing</h1>
    <Toggle on:click={handleClick} {monthly} />
  </header>
  <main class="site-content">
    <div class="wrapper">
      <Card {...basicMonthly} />
      <Card highlight {...proMonthly} />
      <Card {...masterMonthly} />
    </div>
  </main>
</div>
<Footer />

<style>
  .content-wrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  header {
    margin-top: 4rem;
  }
  h1 {
    margin-bottom: 2.5rem;
  }
  @media (min-width: 1050px) {
    header {
      margin: 0;
    }
    h1 {
      margin-bottom: 2rem;
    }
  }
</style>
