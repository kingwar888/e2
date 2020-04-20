<template>
	<view class="warp">
		<view class="example-title">默认样式（3列）</view>
		<view class="example-body">
			<uni-grid :column="3" :highlight="true" @change="change">
				<uni-grid-item v-for="(item, index) in list" :key="index">
					<image :src="item.url" class="image" mode="aspectFill" />
					<text class="text">{{ item.text }}</text>
				</uni-grid-item>
			</uni-grid>
		</view>
		
	</view>
</template>

<script>
	import uniGrid from '../../../src/components/uni-grid/uni-grid.vue'
	import uniGridItem from '../../../src//components/uni-grid-item/uni-grid-item.vue'
	export default {
		components: {
			uniGrid,
			uniGridItem
		},
		data() {
			return {
				list: [{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-1.png',
						text: '新浪'
					},
					{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-2.png',
						text: '微信'
					},
					{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/gird-3.png',
						text: 'QQ'
					},
					{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-6.png',
						text: '抖音'
					},
					{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-7.png',
						text: '百度'
					},
					{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-8.png',
						text: '支付宝'
					},
					{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-9.png',
						text: '字节跳动'
					},
					{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-4.png',
						text: '手机'
					},
					{
						url: 'https://img-cdn-qiniu.dcloud.net.cn/uni-ui/grid-5.png',
						text: '工具'
					}
				]
			}
		},
		methods: {
			change(e) {
				let {
					index
				} = e.detail
				console.log(index)
			}
		}
	}
</script>

<style>
	page {
		display: flex;
		flex-direction: column;
		box-sizing: border-box;
		background-color: #efeff4
	}

	view {
		font-size: 28upx;
		line-height: inherit
	}

	.example {
		padding: 0 30upx 30upx
	}

	.example-title {
		display: flex;
		justify-content: space-between;
		align-items: center;
		font-size: 32upx;
		color: #464e52;
		padding: 30upx 30upx 30upx 50upx;
		margin-top: 20upx;
		position: relative;
		background-color: #fdfdfd;
		border-bottom: 1px #f5f5f5 solid
	}

	.example-title__after {
		position: relative;
		color: #031e3c
	}

	.example-title:after {
		content: '';
		position: absolute;
		left: 30upx;
		margin: auto;
		top: 0;
		bottom: 0;
		width: 6upx;
		height: 32upx;
		background-color: #ccc
	}

	.example .example-title {
		margin: 40upx 0
	}

	.example-body {
		padding: 30upx;
		background: #fff
	}


	.image {
		width: 50upx;
		height: 50upx;
	}

	.text {
		font-size: 26upx;
		margin-top: 10upx;
	}
</style>
