<template>
  <div class="container">
    <FormProgressSection />
    <div class="container-content">
      <div class="container-content-wrapper">
        <FormFieldsSection />
        <MarketingSection />
      </div>
    </div>
    <PhoneSection />
  </div>
</template>

<script>
  import FormProgressSection from './../components/form-container/FormProgressSection'
  import FormFieldsSection from './../components/form-container/FormFieldsSection'
  import MarketingSection from './../components/form-container/MarketingSection'
  import PhoneSection from './../components/form-container/PhoneSection'

  export default {
    components: {
      FormProgressSection,
      FormFieldsSection,
      MarketingSection,
      PhoneSection,
    }
  }
</script>

<style lang="less" scoped>
.container {
  margin: auto;
  max-width: @maxContainerWidth;
  display: grid;

  .container-content {
    background: linear-gradient(to bottom, #fffffa 0% ,#fffffa 20% ,#fefafa 20% ,#fefafa 80%, #ffffff 80%, #ffffff 100%);
    padding: 24px 0px;
  
    .container-content-wrapper {
      display: flex;
      justify-content: space-evenly;
      max-width: 1280px;
      width: 100%;
      margin: auto
    }
  }

  @media (max-width: 1280px) {
    .container-content-wrapper {
      justify-content: space-between !important;
    }
  }

  @media (max-width: 1220px) {
    .container-content-wrapper {
      flex-direction: column;
      align-items: center;
    }
  }
}
</style>
