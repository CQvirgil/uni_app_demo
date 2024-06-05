<template>
	<view class="content">
		<view class="content">
			<image class="logo" src="/static/logo.png"></image>
			
			<input class="input_text" placeholder="请输入用户名" type="text"/>
			<input class="input_text" placeholder="请输入密码" type="safe-password"/>
			<button class="button">登录</button>
			<view id="full">
				<text class="text" id="align-left">注册</text>
				<text class="text" id="align-right">忘记密码</text>
			</view>
		</view>
		<text class="text" id="margin-top">其他登录方式</text>
		<view>
			<image class="logo-sub" src="../../static/wechat_logo.png"/>
			<image class="logo-sub" src="../../static/qq_logo.png"/>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	
	#margin-top{
		margin-top: 24rpx;
	}
	
	#full{
		width: 100%;
	}
	
	#align-right{
		float: right;
		padding-right: 8rpx;
	}
	
	#align-left{
		float: left;
		padding-left: 8rpx;
	}
	
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	
	.logo-sub{
		height: 60rpx;
		width: 60rpx;
		margin-top: 22rpx;
		margin-left: 18rpx;
		margin-right: 18rpx;
	}
	
	.logo {
		height: 100rpx;
		width: 100rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}
	
	.button{
		width: 100%;
		margin: 16rpx;
		color: white;
		background-color: #101405;
	}
	
	.text{
		font-size: 18rpx;
		color: #101405;
		align-items: start;
	}
	
	.bg-border-main{
		
	}
	
	.input_text{
		border: 1rpx;
		border-style: solid;
		border-color: black;
		border-radius: 6rpx;
		padding: 12rpx;
		margin-top: 16rpx;
		font-size: 39rpx;
	}
</style>
