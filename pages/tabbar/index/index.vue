<template>
	<view class="content">
			<!-- 自定义组件 -->
			<navbar></navbar>
			<tab :list="tabList" ></tab>
		</view>
	</view>
</template>

<script>
	//easyCom components/组件名/组件名.vue  局部引入
	import NavBar from '@/components/navbar/navbar.vue'
	import Tab from '@/components/tab/tab.vue'
	export default {
		data() {
			return {
				tabList: []
			}
		},
		components:{
			NavBar,
			Tab
		},
		onLoad() {
           this.getLabel()
		},
		methods: {
           getLabel(){
			   uniCloud.callFunction({
				   name: 'get_label',
				   success(res){
					const { result } =res        
					this.tabList = result.data
					console.log(this.tabList)
				   }
			   })
		   }
		}
	}
</script>

<style>
</style>
