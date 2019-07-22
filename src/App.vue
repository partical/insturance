<template>
  <div id="app">
    <PrimaryPage />
	<Rollup :rollupItems = 'rollupItems'/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import PrimaryPage from './pages/primary/primary.vue';
import Rollup from './components/rollup.vue';

@Component({
  components: {
    PrimaryPage,
	Rollup
  },
})
export default class App extends Vue {

	private data() {
		return {
			rollupItems : [{
				name : '选项1'
			}, {
				name: '选项2'
			}]
		}
	}

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
