<script>
  import Card from './components/Card.svelte';
  import Footer from './components/Footer.svelte';

  // Card details
  const basicMonthly = {
    subLevel: 'Basic',
    price: 19.99,
    storage: 500,
    users: 2,
    sendLimit: 3,
  };
</script>

<main class="site-content">
  <Card {...basicMonthly} />
</main>
<Footer />

<style>
</style>
