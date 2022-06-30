<template>
  <div>
	<table class="border-2">
		<tr>
			<td class="m-2 border-12">
				<b>problem data</b>
			</td>
			<td class="m-2 border-12">
				<b>problem sequence</b>
			</td>
		</tr>
		<tr v-for="data in dataList" v-bind:key="data.id">
			<td>{{data.id}}</td>
			<td>
				<select name="p_seq" id="p_seq">
					<option v-for="item in items" :value="item" :key="item.seq">
						{{item.seq}}
					</option>
				</select>
			</td>
		</tr>
	</table>
  </div>
</template>

<script>

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
	return {
		items: Array.from({length: 10}, (_,idx)=> ({ seq:idx})),
		dataList: Array.from({length: 10}, (_,idx) => ({ id: idx + 1000}))
	}
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .btn {
    @apply font-bold py-2 px-4 rounded;
  }
  .btn-blue {
    @apply bg-blue-500 text-white;
  }
  .btn-blue:hover {
    @apply bg-blue-700;
  }
</style>
