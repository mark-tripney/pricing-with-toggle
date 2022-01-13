<script>
  import Card from "./components/Card.svelte";

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
</script>

<main class="site-content">
<<<<<<< HEAD
  <h1>Our pricing</h1>
  <Toggle on:click={handleClick} {monthly} />
  <Card {...basicMonthly} />
  <div class="highlight">
    <Card {...proMonthly} />
  </div>
  <Card {...masterMonthly} />
</main>
<Footer />

<style>
</style>
=======
  <Card {...basicMonthly} />
  <Card secondary {...proMonthly} />
  <Card {...masterMonthly} />
</main>
>>>>>>> c039f76 (Add unique style to highlighted card.)
