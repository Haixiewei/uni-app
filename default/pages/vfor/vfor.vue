<template>
	<view>
		<view v-for="(stuObj,stuIndex) in studentArray" >
			<view>{{stuIndex}} ：姓名: {{stuObj.name}}, 年龄: {{stuObj.age}}</view>
			<view>
				擅长技能: 
				<!-- <view v-for="sk in stuObj.skill">
					{{sk}},
				</view> -->
				<!-- 会循环3个view 下面block只是内容循环3次 -->
				<block v-for="(sk, skIndex) in stuObj.skill" >
					{{skIndex +':'+ sk}},
				</block>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				studentArray: [
					{
						name: "Jack",
						age: 19,
						skill: ["Java", "Springcloud", "VUE"]
					},
					{
						name: "Steve",
						age: 20,
						skill: ["Java", "HTML", "CSS"],
					},
					{
						name: "Stark",
						age: 18,
						skill: ["CSS", "Springcloud", "VUE"],
					},
					{
						name: "Jason",
						age: 21,
						skill: ["Java", "VUE", "HTML"]
					},
					{
						name: "Lucy",
						age: 16,
						skill: ["VUE", "HTML", "JS"]
					}
				]				
			}
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
