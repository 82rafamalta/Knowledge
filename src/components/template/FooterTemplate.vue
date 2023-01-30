<template>
  <footer class="footer">
    <span>Copyright <strong>Rafa Malta</strong> © 2018-2023</span>
  </footer>
</template>

<script>
export default {
  name: "FooterTemplate",
};
</script>

<style>
.footer {
  grid-area: footer;
  background-color: #ddd;
  color: #333;

  display: flex;
  align-items: center;
  justify-content: flex-end;
  padding-right: 10px;
}
</style>
