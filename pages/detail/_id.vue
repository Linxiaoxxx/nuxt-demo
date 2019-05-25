<template>
	<div class="id">
		<h2>商品详情页</h2>
		<span>{{$route.params.id}}</span>
		<P>{{detail.price}}</P>
		<p>{{detail.description}}</p>
	</div>
</template>

<script>
	import axios from "axios"
	export default{
		async asyncData(){
			const res = await axios.get('/data/test.json');
			return {
				detail: res.data
			}
		}
	}
</script>

<style>
</style>