<template>

  <footer class="w-full h-28 rounded-t-3xl flex flex-col justify-end items-center text-opacity-30 bg-opacity-40 pb-4"
          :class="getCurrentColor">
    <img class="h-16 pt-1 opacity-40" src="../assets/logo-collisa-footer.png" alt="">
    <p>&copy; Lisa Collignon</p>
  </footer>

</template>

<script>
export default {
  name: 'Footer',
  computed: {
    currentRouteName() {
      return this.$route.name;
    },
    getCurrentColor() {
      switch(this.currentRouteName) {
        case "Home":
          return "text-pink-200 bg-purplepink-400";
        case "About":
          return "text-teal-500 bg-teal-500";
        case "Portfolio":
          return "text-white bg-white";
        case "Contact":
          return "text-orange-500 bg-orange-500";
        case "Samenwerking":
          return "text-lime-500 bg-lime-500";
      }
    }
  },
}
</script>
