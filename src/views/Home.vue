<template>
  <div class="home">
    <Homepage msg="SavastaCoffee"/>
    <Maincard/>
  </div>
</template>

<script>
import Homepage from '@/components/Homepage.vue'
import Maincard from '@/components/Maincard.vue'

export default {
  name: 'Home',
  components: {
    Homepage,
    Maincard
  }
}
</script>
