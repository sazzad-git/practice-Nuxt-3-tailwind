<template>
  <div>
    <Head>
      <Title>Nuxt Practice | {{ product.Title }}</Title>
      <Meta name="description" :content="product.description" />
    </Head>
    <ProductDetails :product="product" />
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const url = `https://fakestoreapi.com/products/` + id;

// fetch the product
const { data: product } = await useFetch(url, { key: id });

// if not found 404
if (!product.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "Product not found",
    fatal: true,
  });
}

definePageMeta({
  layout: "products",
});
</script>

<style scoped></style>
