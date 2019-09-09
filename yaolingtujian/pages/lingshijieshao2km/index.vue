<template>
	<view class="content">
		<view class="top">
			灵石介绍
		</view>
		<view style="background-image: url('/static/drawable-xhdpi/INTRODUCTION_Background.png');" class="lingshitupian">
			<view style="background-image: url('/static/drawable-xhdpi/Bubble_Selected.png');" :class="two ? selected: nselected" @click="twoClick">
				2千米灵石
				<view :class="two ? selectedAfter: nselectedAfter">
					<image style="width:100%" v-if="two" src="/static/drawable-xhdpi/2km_Lingshi_Big.png" mode="widthFix"></image>
					<image style="width:100%" v-else src="/static/drawable-xhdpi/2km_Lingshi_Mini.png" mode="widthFix"></image>
				</view>
			</view>
			<view style="background-image: url('/static/drawable-xhdpi/Bubble_Default.png');" :class="five ? selected: nselected" @click="fiveClick">
				5千米灵石
				<view :class="five ? selectedAfter: nselectedAfter">
					<image style="width:100%" v-if="five" src="/static/drawable-xhdpi/5km_Lingshi_Big.png" mode="widthFix"></image>
					<image style="width:100%" v-else src="/static/drawable-xhdpi/5km_Lingshi_Mini.png" mode="widthFix"></image>
				</view>
			</view>
			<view style="background-image: url('/static/drawable-xhdpi/Bubble_Default.png');" :class="ten ? selected: nselected" @click="tenClick">
				10千米灵石
				<view :class="ten ? selectedAfter: nselectedAfter">
					<image style="width:100%" v-if="ten" src="/static/drawable-xhdpi/10km_Lingshi_Big.png" mode="widthFix"></image>
					<image style="width:100%" v-else src="/static/drawable-xhdpi/10km_Lingshi_Mini.png" mode="widthFix"></image>
				</view>
			</view>
		</view>
		<view class="lingshishuju">
			<view style="background-image: url('/static/drawable-xhdpi/Head_Background.png');" class="lingshilist" v-for="(item,index) of spriteData">
				<view>
					<image style="width:100%" :src="item.headImgName" mode="widthFix"></image>
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
				spriteData: sprite.spriteData,
				two: true,
				five: false,
				ten: false,
				selected: 'selected',
				nselected: 'nselected',
				selectedAfter: 'selectedAfter',
				nselectedAfter: 'nselectedAfter',
			}
		},
		onLoad() {
			this.spriteData.forEach(item => {
				item.headImgName = this.sprite.headImgUrl + item.headImgName
			})
		},
		methods: {
			twoClick() {
				this.two = true
				this.five = false
				this.ten = false
			},
			fiveClick() {
				this.five = true
				this.two = false
				this.ten = false
			},
			tenClick() {
				this.ten = true
				this.five = false
				this.two = false
			}
		}
	}
</script>

<style>
	.content {
			display: flex;
			flex-direction: column;
			font-size: 16.66upx;
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
		background-size: cover;
	}
	.selected {
		width: 145.13upx;
		height: 44.44upx;
		background-size: cover;
		position: relative;
		text-align: center;
		line-height: 33upx;
		top:24.3upx;
	}
	.nselected {
		width:111.8upx;
		height: 33.33upx;
		background-size: cover;
		position: relative;
		text-align: center;
		line-height: 27.77upx;
		top:56.25upx;
	}
	.selectedAfter {
		position: relative;
		width:166.66upx;
		height: 220.83upx;
		left:-13.88upx;
		top: 6.94upx;
	}
	.nselectedAfter {
		width:125upx;
		height: 166.66upx;
		position: relative;
		left:-8.33upx;
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
		background-size: cover;
	}
	.lingshilist view {
		width: 100%;
		height: 100%;
		overflow: hidden;
		border-radius: 6944.44rpx;
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
