<template>
	<h1>FulaName: {{ fullName }}</h1>
  </template>

  <script>
  import {ref, computed } from "vue";

  export default {
	setup() {
		const firstName = ref("Yormi");
		const lastName = ref("Altamiranda");
		const fullName = computed(() =>{
			return `${firstName.value} ${lastName.value}`;
		});
		return {
			fullName,
		}
	},
  };
  </script>
