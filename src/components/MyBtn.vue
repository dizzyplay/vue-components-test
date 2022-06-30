<template>
	<button class="btn btn-blue">{{ label }}</button>
</template>

<script>
export default {
	name: "MyBtn",
	props: {
		label: String
	}
}
</script>

<style>
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
