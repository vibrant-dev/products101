<template>
  <div class="container first-container">
    <div class="row">
      <h1>Hi folks</h1>
    </div>
    <div class="row">
      <p>
        We filtered out best e-commerce products in different price ranges for
        India. Those includes laptops, phones and earphones.
      </p>
    </div>
    <div class="row">
      <p>
        <NuxtLink to="/laptops">Best Laptops</NuxtLink> <br />
        <NuxtLink to="/earphones">Best Ear Phones</NuxtLink> <br />
        <NuxtLink to="/phones">Best Phones</NuxtLink> <br />
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#__layout {
  margin-top: 40px;
}

@media (min-width: 1600px) {
  .container,
  .container-sm,
  .container-md,
  .container-lg,
  .container-xl {
    max-width: 1540px;
  }
}
</style>