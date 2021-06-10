<template>
	<view class="content">
			<!-- 自定义组件 -->
			<navbar></navbar>
		</view>
	</view>
</template>

<script>
	//easyCom components/组件名/组件名.vue  局部引入
	import navbar from '@/components/navbar/navbar.vue'
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		components:{
			navbar
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
</style>
