<template>
	<view class="content">
		<!-- <div class="banner">
		    <div class="banner-item" v-for="(item, index) in bannerList" :key="index">
		      <img :src="item.image" class="img" alt="Banner Image">
		    </div>
		  </div> -->
		  
		<div class="top-bar">
			<image class="img-circular" src="../../static/avatar.jpg"></image>
			<div class="top-bar-search">
				<image src="../../static/icons/icon_search.png" class="top-bar-img-seach"></image>
				<input class="top-bar-input" type="text"/>
				<text class="font-nomal">搜索</text>
			</div>
			<image class="img-top-bar-icon" src="../../static/icons/icon_scan.png"></image>
		</div>

		<div class="container">
			<text>body</text>
		</div>

		<div class="bottom-bar">
			<div class="icon" @click="onPickItem(0)">
				<image class="img" src="../../static/icons/icon_home.png"/>
				<text>首页</text>
			</div>
			
			<div class="icon" @click="onPickItem(1)">
				<image class="img" src="../../static/icons/icon_message.png"/>
				<text>消息</text>
			</div>
			
			<div class="icon" @click="onPickItem(2)">
				<image class="img" src="../../static/icons/icon_mine.png"/>
				<text>我的</text>
			</div>
		</div>
	</view>
</template>

<script>
	export default {
		data() {
			return {
			
			}
		},
		methods: {
			onPickItem(index){
				uni.showToast({
					title: '点击' + index,
					icon: 'none',
					duration: 2000
				})
			}
		}
	}
</script>

<style>
	.font-nomal{
		width: 70rpx;
		font-size: 12rpx;
		margin: 12rpx;
	}
	
	.top-bar-input{
		width: 100%;
		height: 100%;
	}
	
	.top-bar-img-seach{
		width: 60rpx;
		height: 50rpx;
		object-fit: cover;
	}
	
	.top-bar{
		width: 100%;
		height: 92rpx;
		border-style: solid;
		border-color: #101405;
		border-width: 1rpx;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
	
	.top-bar-search{
		width: 55%;
		height: 73%;
		background-color: white;
		border-radius: 28rpx;
		display: flex;
		align-items: center;
		padding-left: 12rpx;
		border-color: #101405;
		border-width: 1rpx;
		border-style: solid;
	}
	
	.img-circular{
		width: 60rpx;
		height: 60rpx;
		border-radius: 50%;
		margin-left: 16rpx;
	}
	
	.img-top-bar-icon{
		width: 50rpx;
		height: 50rpx;
		margin-right: 16rpx;
	}
	
	.icon{
		width: 100%;
		font-size: 4upx;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.bottom-bar {
		position: fixed;
		bottom: 0;
		left: 0;
		width: 100%;
		height: 100rpx;
		border-width: 1rpx;
		border-style: solid;
		border-color: #dfdfdf;
		display: flex;
		justify-content: space-around;
		align-items: center;
		flex-direction: row;
	}

	.container {
		width: 100%;
		height: 100%;
		background-color: #dfdfdf;
	}

	.icon{
		width: 100%;
		height: 100%;
	}

	.img {
		width: 50rpx;
		height: 50rpx;
		object-fit: cover;
	}

	.banner {
		width: 96%;
		height: 320rpx;
		overflow: hidden;
		position: relative;
		margin: 8rpx;
		background-color: #dfdfdf;
	}

	.banner-item {
		width: 100%;
		height: 300px;
		position: absolute;
		animation: banner 10s infinite;
	}

	@keyframes banner {
		0% {
			transform: translateX(0);
		}

		20% {
			transform: translateX(-100%);
		}

		40% {
			transform: translateX(-200%);
		}

		60% {
			transform: translateX(-300%);
		}

		80% {
			transform: translateX(-400%);
		}

		100% {
			transform: translateX(0);
		}
	}
</style>