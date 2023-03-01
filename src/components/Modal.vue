<template>
    <div>
	<button class="btn" @click="toggle">Modal</button>
		<teleport to="body">
			<div v-show="show" class="modal">
				<div class="modal-md">
					<div class="modal-header">
						<h1 class="title ">Modal</h1>
						<span class="icon material-symbols-outlined" @click="toggle">
							close
						</span>
					</div>
					<div class="modal-body">
						<div class="">
							<p class="text-1">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nulla doloremque voluptatem saepe necessitatibus vero iure corporis ipsum debitis ea, reiciendis recusandae! Autem, cum dicta nostrum ipsa in maxime facere quod eum laborum voluptas voluptate ducimus quaerat, quis optio. Labore nihil blanditiis tempora harum molestiae eos aspernatur excepturi quis molestias explicabo?</p>
							<button class="btn" @click="toggle">Cerrar</button>
						</div>
					</div>
				</div>
			</div>
		</teleport>
    </div>
</template>

<script>
    export default {
		data(){
			return{
				show: false,
			};
		},
		methods: {
			toggle() {
				this.show = !this.show;
			},
		},
    };
</script>
<style lang="scss">
	.modal{
		font-family: 'Inter', sans-serif;
		// display: none;
		position: fixed; /* Stay in place */
		z-index: 3; /* Sit on top */
		left: 0;
		top: 0;
		width: 100%; /* Full width */
		height: 100%; /* Full height */
		overflow: auto; /* Enable scroll if needed */
		background-color: rgb(0,0,0); /* Fallback color */
		background-color: rgba(0,0,0,0.4); /* Black w/ opacity */


		&-header {
			// padding-bottom: $modal-header-body-padding-x;
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding: 0;
			.title {
				font-size: 1rem;
				font-weight: bold;
				color: #388E3C;

			}
			.icon{
				display: flex;
				align-items: center;
				justify-content: center;
				font-size: 20px;
				cursor: pointer;
				width: 30px;
				height: 30px;
				color: #fff;
				transition: .5s;
				background: #388E3C;
				border-radius: 50%;
				&:hover{
					color: #fff;
					background: #00C853;
					transition: .5s;
				}
			}
		}
		&-body {
			display: flex;
			flex-direction: row;
			justify-content: center;
			align-items: center;
			padding: 0;
			&-img{
				img{
					width: 150px;
					border-radius: 8px;
				}
			}
			&-caption{
				padding: 10px;
			}
			/*@include respond-down("sm"){
				flex-direction: column;
				justify-content: center;
				align-items: center;
				text-align: center;
			}*/
		}
		&-md{
			position: absolute;
			  width: 50%;
			  top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
			background: #f4f4f4;
			border-radius: 8px;
			padding: 10px;
			/*  @include respond-down("sm"){
				width: 100%;
				height: 100%;
			}*/
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
	}


	.reader-only {
    	display: none !important;
	}
	div.reader-only {
    	display: none !important;
	}
	.text-1{
		font-size: 16px;
		line-height: 27px;
		align-items: justify;
		color: #080f08;
	}
</style>
