<template lang="pug">
q-layout(view="lHh Lpr lFf")
  q-page-container
    router-view

</template>

<script>
export default {
  name: "Navbar",
  methods: {
    goTo(id) {
      const element = document.getElementById(id);
      element.scrollIntoView({ behavior: "smooth" });
    },
  },
};
</script>
<style lang="sass" scoped></style>
