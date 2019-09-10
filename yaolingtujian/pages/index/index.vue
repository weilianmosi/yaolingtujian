<template>
	<view class="content">
		<view class="top">
			<view v-if="closeShow" style="position:absolute; top: 2upx; left: 650upx; z-index: 5;font-size: 69.44upx;" @click="close">
				×
			</view>
			<view class="search">
				<input type="search" @confirm="onEnter" @input="handleClose" v-model="value"/>
			</view>
			<view class="nav">
				<view>属性</view>
				<view>图集</view>
				<view>定位</view>
				<view>排序</view>
			</view>
		</view>
		<view v-if="search" class="contain">
			<view style="background-image: url('/static/drawable-xhdpi/ILLUSTRATION_Card_Background.png')" 
				class="imgshow" v-for="(item,index) of filterSpriteData" @click="toClick(item)">
					<view class="mainImg">
						<image style="width:100%" class="image"  :data-index="index" :src="(sprite.bodyImgUrl + item.bodyImgName)" mode="widthFix"></image>
					</view>
					<view class="characteristic">
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
		<view v-else class="contain">
			<view style="background-image: url('/static/drawable-xhdpi/ILLUSTRATION_Card_Background.png')" 
				class="imgshow" v-for="(item,index) of spriteData" @click="toClick(item)">
					<view class="mainImg">
						<image style="width:100%" class="image" :class="{lazy:!item.show}" :data-index="index" :src="item.show ? (sprite.bodyImgUrl + item.bodyImgName):''" mode="widthFix"></image>
					</view>
					<view class="characteristic">
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
	</view>
</template>

<script>
	import sprite from '../../yaolingtujian.json';
	export default {
		data() {
			var spriteData = []
			spriteData = sprite.spriteData.map(item => {
				item.show = false
				// item.bodyImgName = sprite.bodyImgUrl + item.bodyImgName
				return item
			})
			return {
				windowHeight: 0,
				sprite: sprite,
				spriteData: spriteData,
				show: false,
				search: false,
				closeShow: false,
				imgLoad: true,
				filterSpriteData: [],
				value: '',
			}
		},
		onLoad() {
			// console.log(sprite.bodyImgUrl, this.spriteData[0].show, this.spriteData[0].bodyImgName)
			this.windowHeight = uni.getSystemInfoSync().windowHeight
		},
		methods: {
			load() {
				uni.createSelectorQuery().selectAll('.lazy').boundingClientRect((images) => {
					images.forEach((image, index) => {
						if (image.top <= this.windowHeight) {
							this.spriteData[image.dataset.index].show = true;
						}
					})
				}).exec()
			},
			onEnter(event) {
				event.preventDefault(); 
				this.search = true
				this.filterSpriteData = this.spriteData.filter(item => {
					if(item.name.includes(event.target.value)) {
						return item 
					}
				})
			},
			handleClose(event) {
				if(event.target.value) {
					this.closeShow = true
				}
			},
			close() {
				this.search = false 
				this.closeShow = false
				this.value = ''
			},
			toClick(item) {
				var id = item.id
				uni.navigateTo({
				    url: `../imgDetail/index?id=${id}`
				});
			}
		},
		onShow() {
			if (!this.show) {
				this.show = true
				setTimeout(() => {
					this.load()
				}, 150)
			}
		},
		onPageScroll() {
			this.load()
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
	image {
		will-change: transform;
	}
	.image {
		position: relative;
	}
	.top {
		position: relative;
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
		padding: 17.36upx 0upx 18.75upx 27.08upx;
		flex-direction: row;
		flex-wrap:wrap;
		background-color: #f7f7f7;
	}
	.imgshow {
		background-size: cover;
		border-radius: 13.88upx;
		border:solid black 0.69upx;
		width:214.58upx;
		height: 292.36upx;
		margin-top: 14.58upx;
		margin-right: 24upx;
		position: relative;
	}
	.mainImg {
		width:214.58upx;
		position: relative;
	}
	.name {
		font-size: 25upx;
		text-align: center;
		color: #666666;
		margin:22.91upx;
	}
	.footer {
		text-align: center;
		font-size: 25upx;
		margin-bottom: 17.36upx;
	}
	.characteristic {
		position: absolute;
		width:38.88upx;
		height: 38.88upx;
		top:11.11upx;
		left:11.11upx;
	}
	.characteristic img {
		width:38.88upx;
		height: 38.88upx;
	}
</style>
