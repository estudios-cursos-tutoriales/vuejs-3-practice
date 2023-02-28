<template>
	<div>
		<Modal />
	</div>
</template>

<script>
import Modal from "./components/Modal.vue";
export default {
	name: "App",
	components: {
		Modal,
	},
};
</script>

<style lang="scss">
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
	.btn{
		outline: none;
		padding: 8px 30px;
		border-radius: 4px;
		border: 1px solid #28692b;
		background: #388E3C;
		color: #fff;
		font-family: 'Inter', sans-serif;
		cursor: pointer;
		transition: .5s ease;
		&:hover{
			border: 1px solid #37943c;
			background: #245026;
		}
	}

</style>
