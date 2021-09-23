<template>
	<div class="counter-container">
		<div class="counter">
			<img src="@/assets/coffee.svg" alt="Coffee" class="icon">
			<h3 id="counter" :data-target="counter" class="count">0</h3>
			<h6>Cups of Coffee</h6>
		</div>
	</div>
</template>

<script>
import axios from 'axios'
export default {
  name: 'Counter',
  data: function(){
    return {
      counter: 0
    }
  },
  methods: {
    updateDataTarget(){
      const data_request = {operation: 'get_today_coffee'};
      axios.post('http://localhost:8888', data_request)
        .then(response => (this.counter = response.data.counter));
    },
    counterAnimation() {
      const counter = document.getElementById("counter");

      const counterAnimation = () => {
        const target = this.counter;
        const count = parseInt(+counter.innerText);

        if (count < target) {
          counter.innerText = count + 1;
          setTimeout(counterAnimation, 200);
        } else {
          counter.innerText = target;
        }
      };
      counterAnimation();
    }
  },
  mounted(){
    this.updateDataTarget()
  },
  updated(){
    this.counterAnimation()
  }
}
</script>

<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.container {
  width: 80%;
  margin: auto;
}

.heading {
  text-align: center;
  font-size: 3.5rem;
  font-weight: bold;
  padding: 1rem 0;
}

.counter-container {
  display: flex;
  justify-content: center;
  align-items: center;
}

.counter {
  text-align: center;
}

.counter h3 {
  padding: 0.5rem 0;
  font-size: 2.5rem;
  font-weight: 800;
}

.counter h6 {
  font-size: 2rem;
  padding-bottom: 1rem;
}


h6 {
	display: block;
	font-size: 0.67em;
	margin-inline-start: 0px;
	margin-inline-end: 0px;
	font-weight: bold;
}


.icon {
  height: auto;
  width: 5rem;
}

.main_image {
  max-width: 20rem;
}
</style>