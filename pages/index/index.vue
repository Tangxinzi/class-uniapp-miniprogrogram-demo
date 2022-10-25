<template name="demo">
	<view class="content">
		<image class="logo" :src="logo"></image>
		<view class="text-area">
			<text>{{ title }}</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				logo: '/static/logo.png',
				title: 'Hello',
				items: [{
						value: '🍎'
					},
					{
						value: '🍌'
					},
					{
						value: '🍓'
					}
				]
			}
		},
		onLoad() {

		},
		methods: {
			print(data) {
				// this.data.title 小程序取值
				console.log(this.title + ' ' + data)
			}
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
