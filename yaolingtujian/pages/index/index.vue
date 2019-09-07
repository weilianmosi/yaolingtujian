<template>
	<view class="content">
		<view class="top">
			<view class="search">
				<input type="text"  value="" />
			</view>
			<view class="nav">
				<view>属性</view>
				<view>图集</view>
				<view>定位</view>
				<view>排序</view>
			</view>
		</view>
		<view class="contain">
			<view class="imgshow" v-for="(item,index) of spriteData">
					<view class="mainImg">
						<img style="width:100%;" v-bind:src= "item.bodyImgName">
					</view>
					<view class="characteristic" >
						<img v-if="item.fiveEle[0] ==='金'" src="/static/drawable-xhdpi/Property_40px_Jin.png" mode="">
						<img v-else-if="item.fiveEle[0] ==='木'" src="/static/drawable-xhdpi/Property_40px_Mu.png" mode="">
						<img v-else-if="item.fiveEle[0] ==='水'" src="/static/drawable-xhdpi/Property_40px_Shui.png" mode="">
						<img v-else-if="item.fiveEle[0] ==='火'" src="/static/drawable-xhdpi/Property_40px_Huo.png" mode="">
						<img v-else-if="item.fiveEle[0] ==='土'" src="/static/drawable-xhdpi/Property_40px_Tu.png" mode="">
						<img v-else-if="item.fiveEle[0] ==='无'" src="/static/drawable-xhdpi/Property_40px_Wu.png" mode="">
						<img v-else-if="item.fiveEle[0] ==='鬼'" src="/static/drawable-xhdpi/Property_40px_Gui.png" mode="">
					</view>
					<view class="name">
						{{item.name}}
					</view>
			</view>
		</view>
		<view class="footer">
			<view>正在努力加载中......</view>
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
					item.bodyImgName = this.sprite.bodyImgUrl + item.bodyImgName
				})
			},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		font-family: "Source Han Sans CN";
		color:#666;
	}
	.top {
		background-image: url("/static/drawable-xhdpi/妖灵图鉴最上底色图.png");
	}
	.search {
		width:705.55upx;
		margin:18.75upx 15.97upx 15.27upx;
		height:55.55upx;
		border: solid 0.69upx #333333;
		border-radius: 10.41upx;
		background-color: #fff;
	}
	.nav {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
	}
	.nav view {
		width: 177.77upx;
		height: 63.88upx;
		xbackground-image: url("/static/drawable-xhdpi/ILLUSTRATION_Arrow_Under.png");
		xbackground-position-x: 70%;
		xbackground-position-y: 50%;
		xbackground-repeat: no-repeat;
		font-size: 25upx;
		line-height: 63.88upx;
		background-color: #fff;
		text-align: center;
		border: solid #666 0.69upx;
		border-top-left-radius: 13.88upx;
		border-top-right-radius: 13.88upx;
	}
	.contain {
		display: flex;
		padding: 17.36upx 27.08upx 18.75upx 27.08upx;
		flex-direction: row;
		flex-wrap:wrap;
		justify-content: space-between;
		background-color: #f7f7f7;
	}
	.imgshow {
		background-image: url("/static/drawable-xhdpi/ILLUSTRATION_Card_Background.png");
		background-size: cover;
		border-radius: 13.88upx;
		border:solid black 0.69upx;
		width:214.58upx;
		height: 292.36upx;
		margin-top: 14.58upx;
		position: relative;
	}
	.mainImg {
		width: 100%;
	}
	.name {
		font-size: 25upx;
		text-align: center;
		color: #666666;
		margin:13.88upx;
	}
	.footer {
		text-align: center;
		font-size: 25upx;
		margin-bottom: 17.36upx;
	}
	.characteristic {
		position: absolute;
		xbackground-image: url("/static/drawable-xhdpi/Property_40px_Jin.png");
		xbackground-size: cover;
		width:38.88upx;
		height: 38.88upx;
		top:11.11upx;
		left:11.11upx;
	}
	.characteristic img {
		width: 100%;
	}
</style>
