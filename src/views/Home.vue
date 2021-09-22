<template>
  <div class="home">
    <Homepage msg="SavastaCoffee"/>
    <Counter/>
  </div>
</template>

<script>
import Homepage from '@/components/Homepage.vue'
import Counter from '@/components/Counter.vue'

export default {
  name: 'Home',
  components: {
    Homepage,
    Counter
  }
}
</script>
