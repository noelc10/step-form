<template>
  <div class="phone-section">
    <p>Do you want to speak to someone immediately?</p>
    <h1>0800-PHONE-ME</h1>
  </div>
</template>

<script>
  export default {}
</script>

<style lang="less" scoped>
  .phone-section {
    max-width: 1280px;
    width: 100%;
    margin: auto;
    padding: 0 32px;

    p,
    h1 {
      margin: 8px 0;
    }
  }

  @media (max-width: 1280px) {
    .phone-section {
      padding: 0 !important;
    }
  }
</style>
