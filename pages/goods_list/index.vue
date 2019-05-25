<template>
	<div class="goodslist">
		<h2>商品列表</h2>
		<ul>
			<li v-for="item in list" :key="item.name">
				<nuxt-link :to="'/detail/' + item.id">{{item.name}}</nuxt-link>
			</li>
		</ul>
	</div>
</template>

<script>
	export default{
		data:() => {
			return{
				list:[
					{id: '009', name:'iphone20', price:20000},
					{id: '001', name:'huawei' , price: 8000},
					{id: '007', name: 'cuizi' , price:5000}
				]
			}
		}
	}
</script>

<style>
</style>