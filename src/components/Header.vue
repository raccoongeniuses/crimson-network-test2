<template>
  <header>
    <h1>{{ title }}</h1>
    <Button text="Tambah Buku" color="green" />
    <Button text="Update List" color="blue" />
    <Button text="Delete Buku dalam List" color="red" />
  </header>
</template>

<script>
import Button from "./Button";
export default {
  name: "HeaderComponent",
  props: {
    title: {
      type: String,
    },
  },
  components: {
    Button,
  },
};
</script> 
// scoped : berlaku di dokumen ini 
<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style> 