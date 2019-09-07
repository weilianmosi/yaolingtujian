<template>
	<view class="content">
		<view class="top">
			灵石介绍
		</view>
		<view class="lingshitupian">
			<view class="two">
				2千米灵石
			</view>
			<view class="five">
				5千米灵石
			</view>
			<view class="ten">
				10千米灵石
			</view>
		</view>
		<view class="lingshishuju">
			<view class="lingshilist" v-for="(item,index) of spriteData">
				<view>
					<img :src="item.headImgName" alt="">
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import sprite from '../../yaolingtujian.json'
	export default {
		data() {
			return {
				sprite: sprite,
				spriteData: sprite.spriteData 
			}
		},
		onLoad() {
			this.spriteData.forEach(item => {
				item.headImgName = this.sprite.headImgUrl + item.headImgName
			})
		},
		methods: {
			// dayin(e) {
			// 	console.log('aaa')
			// },
		}
	}
</script>

<style>
	.content {
			display: flex;
			flex-direction: column;
			font-size: 16.66upx;
			/* align-items: center;
			justify-content: center; */
			xbackground-image: url('/static/drawable-xhdpi/INTRODUCTION_Background.png');
			xbackground-size: cover;
			
		}
	.top {
		height:88.88upx;
		width: 100%;
		font-size: 41.66upx;
		text-align: center;
		line-height: 88.88upx;
		color: #f2f2f2;
		background-image: url('/static/drawable-xhdpi/Back.png');
		background-repeat: no-repeat;
		background-position-x: 27.08upx;
		background-position-y: 20.83upx;
		background-color: green;
	}
	.lingshitupian {
		height: 329.86upx;
		width: 100%;
		padding-left:54.86upx;
		padding-right: 72.22upx;
		display: flex;
		flex-direction: row;
		box-sizing: border-box;
		justify-content: space-between;
		background-image: url('/static/drawable-xhdpi/INTRODUCTION_Background.png');
		background-size: cover;
	}
	.ten {
		width: 145.13upx;
		height: 44.44upx;
		background-image: url('/static/drawable-xhdpi/Bubble_Selected.png');
		background-size: cover;
		position: relative;
		text-align: center;
		line-height: 33upx;
		top:24.3upx;
	}
	.five {
		width:111.8upx;
		height: 33.33upx;
		background-image: url('/static/drawable-xhdpi/Bubble_Default.png');
		background-size: cover;
		position: relative;
		text-align: center;
		line-height: 27.77upx;
		top:56.25upx;
	}
	.two {
		width:111.8upx;
		height: 33.33upx;
		text-align: center;
		line-height: 27.77upx;
		background-image: url('/static/drawable-xhdpi/Bubble_Default.png');
		background-size: cover;
		position: relative;
		top:56.25upx;
	}
	.five::after {
		content: '';
		display: block;
		width:125upx;
		height: 166.66upx;
		background-image: url('/static/drawable-xhdpi/5km_Lingshi_Mini.png');
		background-size: cover;
		position: relative;
		left:-8.33upx;
		top: 6.94upx;
	}
	.two::after {
		content: '';
		display: block;
		position: relative;
		width:125upx;
		height: 166.66upx;
		background-image: url('/static/drawable-xhdpi/2km_Lingshi_Mini.png');
		background-size: cover;
		position: relative;
		left:-8.33upx;
		top: 6.94upx;
	}
	.ten::after {
		content: '';
		display: block;
		position: relative;
		width:166.66upx;
		height: 220.83upx;
		background-image: url('/static/drawable-xhdpi/10km_Lingshi_Big.png');
		background-size: cover;
		left:-13.88upx;
		top: 6.94upx;
	}
	.lingshishuju {
		box-sizing: border-box;
		width: 100%;
		padding-left: 1.38upx;
		padding-right:8.33upx;
		display: flex;
		flex-direction: row;
		flex-wrap:wrap;
	}
	.lingshilist {
		width: 117.36upx;
		height: 117.36upx;
		margin: 47.91upx 33.33upx 0;
		background-image: url('/static/drawable-xhdpi/Head_Background.png');
		background-size: cover;
		
	}
	.lingshilist view {
		width: 100%;
		height: 100%;
		overflow: hidden;
		border-radius: 6944.44rpx;
	}
	.lingshilist img {
		width: 100%;
	}
	.lingshilist::after {
		content: '小浣熊';
		display: block;
		position: relative;
		width: 88.88upx;
		height: 27.77upx;
		background-color: #95dcdc;
		border-radius: 8px;
		text-align: center;
		line-height: 27.77upx;
		top: 6.25upx;
		left: 14.23upx;
	}
</style>
