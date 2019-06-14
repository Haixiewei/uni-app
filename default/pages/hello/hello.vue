<template>
	<navigator url="../index/index" open-type="navigateBack">
		<view>
			<view class="green" style="width: 750upx;height: 750upx;"></view>
		</view>
	</navigator>

</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onLoad() {
			console.log("页面加载")
		},
		onShow() {
			console.log('页面show')
		},
		onReady() {
			console.log("页面初次渲染完成")
		},
		onUnload() {
			console.log("页面关闭")
		},
		onHide() {
			console.log('页面Hide')
		},
		onShareAppMessage() {
			console.log('分享')
		},
		onPageScroll() {
			console.log('页面滚动')
		},
		onBackPress() {
			console.log('页面返回')
		},
		
		methods: {
			
		}
	}
</script>

<style>
	.green{
		background-color: green;
	}
</style>
