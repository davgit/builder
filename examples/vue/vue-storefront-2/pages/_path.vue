<template>
  <div id="home">
    <BuilderContent />
  </div>
</template>
<script>
import Vue from 'vue';
import cacheControl from '../helpers/cacheControl';

export default Vue.extend({
  name: 'Home',
  middleware: cacheControl({
    'max-age': 60,
    'stale-when-revalidate': 5,
  }),
});
</script>

<style lang="scss" scoped>
#home {
  box-sizing: border-box;
  padding: 0 var(--spacer-sm);
  @include for-desktop {
    max-width: 1240px;
    padding: 0;
    margin: 0 auto;
  }
}
</style>
