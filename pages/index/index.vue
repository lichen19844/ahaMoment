<template>
	<view class="content">
		<view class="top-bar">
			<view class="top-bar-left"><image src="../../static/images/img/one.png"></image></view>
			<view class="top-bar-center"><image src="../../static/images/index/logo.png"></image></view>
			<view class="top-bar-right">
				<view class="search"><image src="../../static/images/index/search.png"></image></view>
				<view class="add"><image src="../../static/images/index/add.png"></image></view>
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
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;
	// width: 750rpx;
}

.top-bar {
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
			width:68rpx;
			height:68rpx;
			border-radius:16rpx;
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
</style>
