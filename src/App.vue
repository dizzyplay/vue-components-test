<template>
  <div id="app" class="flex flex-col ">
	<div class="absolute top-0 right-0 w-32 p-4 border-4 h-22 box-border">
		<select name="st_group" id="st_group">
			<option v-for="g in stGroup" :item="g.name" :key="g.name">
				{{ g.name }}
			</option>
		</select>
	</div>
	<div>
		<TableView/>
	</div>
  </div>
</template>

<script>
import TableView from './components/TableView.vue'

const g = ['very_high','high','middle','low','very_low'];

export default {
  name: 'App',
  components: {
    TableView
  },
  data() {
	return {
		stGroup: Array.from({length: 5} ,(_,idx) => ({ name: g[idx]}))
	}
  }
}
</script>

<style>
#app {
  margin-top: 60px;
}
</style>
