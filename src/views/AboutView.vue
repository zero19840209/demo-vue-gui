<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  <BaseCard></BaseCard>
</template>
<script>
// @ is an alias to /src
import BaseCard from '@/components/BaseCard.vue'

export default {
  name: 'AboutView',
  components: {
    BaseCard
  }
}
</script>
