<template>
  <div>
    <h2>About</h2>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Provident atque
      repellat rerum quisquam ipsam tempore fuga, quaerat, unde animi facilis
      corporis. Aliquam recusandae optio cupiditate officiis inventore
      repudiandae facilis hic, voluptatibus labore dolor architecto sunt
      sapiente perspiciatis nemo sed nobis veritatis deleniti laboriosam
      reiciendis accusantium incidunt. Minus dignissimos saepe quia.
    </p>
    <div>{{ data }}</div>
  </div>
</template>

<script setup>
// api dynamic data
const { data } = await useFetch("/api/currency/GBP");

// api data
// const { data } = await useFetch("/api/practice");

// send query params
// const { data } = await useFetch("/api/practice?name=mario", {
//   method: "post",
//   body: { age: 30 },
// });
</script>

<style scoped>
h2 {
  margin-bottom: 20px;
  font-size: 36px;
}
p {
  margin: 20px 0;
}
</style>
