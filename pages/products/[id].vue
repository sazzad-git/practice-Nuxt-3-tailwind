<template>
  <div>
    <p>Product details for {{ id }}</p>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nemo, quisquam
      dolore repellat amet suscipit tempore iste ipsa, soluta consequatur saepe
      tenetur voluptatibus. Tempora quas magnam odio repellendus illum debitis?
      Modi dicta odit, minima aspernatur iusto labore, neque, sequi voluptatem
      iure amet totam dignissimos nobis iste suscipit molestias fuga impedit
      dolorem.
    </p>
  </div>
</template>

<script setup>
const { id } = useRoute().params;
definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>
