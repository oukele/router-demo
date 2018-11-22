<template>
	<!-- <div id="app">
		<div id="nav">
			<router-link to="/">Home</router-link> |
			<router-link to="/about">About</router-link>
		</div>
		<router-view />
	</div> -->
	<!-- 使用组件 -->
	<HelloWord></HelloWord>
</template>


<script>
	//导入组件
	import HelloWord from './components/HelloWorld.vue'
	export default {
			components:{//注册组件
				HelloWord
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
