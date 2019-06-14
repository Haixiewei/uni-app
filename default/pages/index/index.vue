<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		
		<view>
			<text class="title">{{title}}\n</text>
			<text class="title">{{title + ' very good'}}</text>
			<input type="text" :value="title" @input="change"/>
		</view>
		
		<!-- <view><br/></view> -->
		
		<navigator :url="url"> <!-- 错误写法：url="{{url}}" -->
			<view>
				I am {{student.age >= 18 ? '成年' : '未成年'}} . <br/>
				I have skills such as: {{skill[0]}},{{skill[1]}},{{skill[2]}},{{skill[3]}},{{skill[4]}}
			</view>
		</navigator>
		
		<navigator url="../events/events">
			<view class="title">
				events 常见事件处理
			</view>
		</navigator>
		
		<navigator url="../vif/vif">
			<view class="title">
				vif 条件渲染
			</view>
		</navigator>
		
		<navigator url="../vfor/vfor">
			<view class="title">
				vfor 列表渲染
			</view>
		</navigator>

		<navigator url="../vforkey/vforkey">
			<view class="title">
				vforkey 保证组件和数据捆绑唯一
			</view>
		</navigator>
		
		<navigator url="../ifCompile/ifCompile">
			<view class="title">
				ifCompile 条件编译
			</view>
		</navigator>
		
		<navigator url="../flex/flex-direction/flex-direction">
			<view class="title">
				flex 容器中 flex 成员项的排列方向
			</view>
		</navigator>
		
		<navigator url="../flex/flex-wrap/flex-wrap">
			<view class="title">
				flex 换行 flex-wrap
			</view>
		</navigator>
		
		<navigator url="../flex/justify-content/justify-content">
			<view class="title">
				设置元素在主轴上的对齐方式
			</view>
		</navigator>
		
		<navigator url="../flex/align-items/align-items">
			<view class="title">
				容器元素在交叉轴上的对齐方式
			</view>
		</navigator>
		
		<navigator url="../flex/align-content/align-content">
			<view class="title">
				设置轴线的对齐方式
			</view>
		</navigator>
		
		<navigator url="../flex/flex-items/flex-items">
			<view class="title">
				容器元素的属性
			</view>
		</navigator>
		
		<navigator url="../flex/align-self/align-self">
			<view class="title">
				重写容器中元素在交叉轴上的对齐方式
			</view>
		</navigator>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello1',
				student: {
					age: 17
				},
				skill: ["Java", "HTML", "CSS", "Springcloud", "VUE"],
				url: "../hello/hello",
				image: ""
			}
		},
		onLoad() {

		},
		methods: {
			change(e){
				var txtTitle = e.detail.value;
				this.title = txtTitle;
			}
		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 400upx;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
