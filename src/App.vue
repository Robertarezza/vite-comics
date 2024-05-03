<script >
import AppHeader  from './components/AppHeader.vue'
import AppMain  from './components/AppMain.vue'
import AppFooter  from './components/AppFooter.vue'
import IconList  from './components/IconList.vue'

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
    IconList,
  },
  data() {
    return {};
  },
};
</script>


<template>
 
  <AppHeader />
  <AppMain />
  <IconList />
  <AppFooter />
</template>

<style lang="scss">

</style>
