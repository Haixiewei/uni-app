<template>
	<view>
	
		<view v-if="isShow">
			now you see me
		</view>
		<view v-else>
			miss
		</view>
		<!-- v-if v-show 的区别：前者是否会在dom中被移除，后者 display:none -->
		<view v-show="isShow">
			now you see me
		</view>
		
		<!-- 三元计算 -->
		<view v-if="sex1 == 1 ? true : false">
			男性
		</view>
		<view v-if="sex0 == 0 ? true : false">
			女性
		</view>
		
		<view>
			========================
		</view>
		
		<view v-if="sex1 == 1">
			男性
		</view>
		<view v-else-if="sex1 == 0">
			女性
		</view>
		<view v-else>
			未知
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isShow: false,
				sex0: 0,
				sex1: 1
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
