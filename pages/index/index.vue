<template>
	<view class="content">
		<!-- 首页 -->
		<!-- 顶部 -->
		<view class="top-bar">
			<view class="top-bar-left"><image src="../../static/images/img/one.png"></image></view>
			<view class="top-bar-center"><image src="../../static/images/index/logo.png"></image></view>
			<view class="top-bar-right">
				<view class="search"><image src="../../static/images/index/search.png"></image></view>
				<view class="add"><image src="../../static/images/index/add.png"></image></view>
			</view>
		</view>
		<view class="main">
			<!-- 好友请求 -->
			<!-- <view class="apply"></view> -->
			<!-- 模拟好友申请 -->
			<view class="friends">
				<view class="friend-list">
					<view class="friend-list-l">
						<text class="tip">1</text>
						<image src="../../static/images/index/apply.png" mode=""></image>
					</view>
					<view class="friend-list-r">
						<view class="top">
							<view class="name">香果果</view>
							<view class="time">10:36</view>
						</view>
						<view class="news">久仰大名，我们可以一起讨论vue和react大前端的实验呀！</view>
					</view>
				</view>
			</view>
			<!-- 聊天列表 -->
			<view class="friends">
				<view class="friend-list">
					<view class="friend-list-l">
						<text class="tip">1</text>
						<image src="../../static/images/img/five.png" mode=""></image>
					</view>
					<view class="friend-list-r">
						<view class="top">
							<view class="name">椰椰酱</view>
							<view class="time">11:59</view>
						</view>
						<view class="news">哥老关真好吃，我们什么时候再一起去吃呀？</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {};
	},
	onLoad() {},
	methods: {}
};
</script>

<style lang="scss">
.content {
	// display: flex;
	// flex-direction: column;
	// align-items: center;
	// justify-content: center;
	width: 750rpx;
}

// 首页顶部
.top-bar {
	z-index: 100;
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 88rpx;
	background: $uni-bg-color;
	// box-shadow: 0px 1px 0px 0px rgba(0, 0, 0, 0.1);
	border-bottom: 1px solid $uni-border-color;
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
	.top-bar-left {
		// float: left;
		image {
			padding: 10rpx $uni-spacing-col-base 0;
			width: 68rpx;
			height: 68rpx;
			border-radius: 16rpx;
		}
	}
	.top-bar-center {
		image {
			padding-top: 16rpx;
			width: 88rpx;
			height: 42rpx;
		}
	}
	.top-bar-right {
		padding-top: 10rpx;
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		align-items: center;
		.search image {
			width: 52rpx;
			height: 52rpx;
		}
		.add image {
			padding: 0 $uni-spacing-col-base;
			width: 48rpx;
			height: 48rpx;
		}
	}
}

// 聊天列表
.main {
	padding: 88rpx $uni-spacing-col-base;
	border: 1px solid red;
}
.main .friend-list {
	display: flex;
	flex-direction: row;
	justify-content: space-between;
	align-items: center;
	width: 100%;
	// height: 128rpx;
	// line-height: 128rpx;
	height: 96rpx;	// 技巧：和图片高度一样，再设置上下padding
	padding: 16rpx 0;
	border: 1px solid;
	.friend-list-l {
		position: relative;
		border: 1px solid;
		.tip {
			position: absolute;
			z-index: 100;
			min-width: 36rpx; //自适应
			height: 36rpx;
			line-height: 36rpx;
			text-align: center;
			top: 0rpx;
			left: 68rpx;
			background: $uni-color-warning;
			border-radius: $uni-border-radius-circle;
			font-size: $uni-font-size-sm;
			color: $uni-text-color-inverse;
		}
		image {
			top: 6rpx;
			width: 96rpx;
			height: 96rpx;
			border-radius: $uni-border-radius-base;
			background-color: $uni-color-primary;
		}
	}
	.friend-list-r {
		flex: 1;
		border: 1px solid blue;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: flex-start;
		padding-left: 32rpx;
		width: 100%;
		.top {
			border: 1px solid;
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
			width: 100%;
			height: 50rpx;
			line-height: 50rpx;
			.name {
				font-size: 36rpx;
				font-weight: 400;
				color: $uni-text-color;
				line-height: 50rpx;
			}
			.time {
				font-size: $uni-font-size-sm;
				font-weight: 400;
				color: $uni-text-color-disable;
				line-height: 50rpx;
				padding-bottom: 4rpx;
			}
		}
		.news {
			border: 1px solid red;
			width: 100%;
			font-size: $uni-font-size-base;
			color: $uni-text-color-grey;
			line-height: 40rpx;
			// 省略号处理方法
			display: -webkit-box;
			-webkit-box-orient: vertical;
			-webkit-line-clamp: 1;
			overflow: hidden;
		}
	}
}
</style>
