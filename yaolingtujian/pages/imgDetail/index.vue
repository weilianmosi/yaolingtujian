<template>
	<view style="background-image: url('/static/drawable-xhdpi/ILLUSTRATION_Background.png');" class="content">
		<view class="top">
			<view>妖灵图鉴</view>
		</view>
		<view class="detail">
			<view class="left">
				<image style="width:100%" src="/static/drawable-xhdpi/ILLUSTRATION_Arrow_Left.png" mode="widthFix"></image>
			</view>
			<view class="detailimg">
				<image style="width:100%" src="http://hy.gwgo.qq.com/sync/pet/512_body/5_XiaoHuanXiong_big.png" mode="widthFix"></image>
			</view>
			<view class="right">
				<image style="width:100%" src="/static/drawable-xhdpi/ILLUSTRATION_Arrow_Right.png" mode="widthFix"></image>
			</view>
		</view>
		<view class="introduction">
			<view class="data">
				<view class="datatitle">
					<view class="segmentation">
						<view class="leftcircle">
						</view>
						<view class="dashed"></view>
						<view class="rightcircle">
						</view>
					</view>
					<view class="title">
						妖灵数据<text style="font-size: 25upx; color:#666;">(资质32)</text>
					</view>
				</view>
				<view class="grade">
					<view class="now">
						<view class="lowest">当前</view>
						<view class="jishu">
							(LV:1)
						</view>
					</view>
					<view class="circle">
					</view>
					<view class="line">
					</view>
					<view class="highest">
						最高
						<view class="jishu">
							(LV:20)
						</view>
					</view>	
				</view>
				<view class="parameter">
					<view class="picture">
						<view>
							<image class="img1" src="/static/drawable-xhdpi/ILLUSTRATION_physical_attack_Icon.png" mode="widthFix"></image>
						</view>
						<view>
							<image class="img2" src="/static/drawable-xhdpi/ILLUSTRATION_Physical_defense_Icon.png" mode="widthFix"></image>
						</view>
						<view>
							<image class="img3" src="/static/drawable-xhdpi/ILLUSTRATION_Spell_attacks_Icon.png" mode="widthFix"></image>
						</view>
						<view>
							<image  class="img4" src="/static/drawable-xhdpi/ILLUSTRATION_Spell_defense_Icon.png" mode="widthFix"></image>
						</view>
						<view>
							<image  class="img5" src="/static/drawable-xhdpi/ILLUSTRATION_health_point_Icon.png" mode="widthFix"></image>
						</view>
					</view>
					<view class="description">
						<view>
							物攻
						</view>
						<view>
							物防
						</view>
						<view>
							法攻
						</view>
						<view>
							法防
						</view>
						<view>
							生命
						</view>
					</view>
					<view class="schedule">
						<view class="wugong">
							 <progress percent="20" activeColor="#6fdee7" backgroundColor="#4c4c4c" stroke-width="21"/>
						</view>
						<view class="wufang">
							 <progress percent="3" activeColor="#6fdee7" backgroundColor="#4c4c4c" stroke-width="21"/>
						</view>
						<view class="fagong">
							 <progress percent="14" activeColor="#6fdee7" backgroundColor="#4c4c4c" stroke-width="21"/>
						</view>
						<view class="fafang">
							 <progress percent="18" activeColor="#6fdee7" backgroundColor="#4c4c4c" stroke-width="21"/>
						</view>
						<view class="life">
							 <progress percent="23" activeColor="#6fdee7" backgroundColor="#4c4c4c" stroke-width="21"/>
						</view>
					</view>
					<view class="digital">
						<view class="digital1">
							246
						</view>
						<view class="digital2">
							285
						</view>
						<view class="digital3">
							246
						</view>
						<view class="digital4">
							300
						</view>
						<view class="digital5">
							1035
						</view>
					</view>
				</view>
				<view class="specific">
					<view class="datatitle" style="position: relative; top: 118.05upx">
						<view class="segmentation">
							<view class="leftcircle">
							</view>
							<view class="dashed"></view>
							<view class="rightcircle">
							</view>
						</view>
						<view class="retitle">
							克制关系
						</view>
					</view>
					<view class="relationship">
						<view class="restraintAttr">
							<view class="restrain">
								克制
							</view>
							<view class="resimg">
								<view style="width:55.55upx;">
									<image style="width:100%;" src="/static/drawable-xhdpi/Property_80px_Shui.png" mode="widthFix"></image>
								</view>
								<view style="width:55.55upx; margin-left: 11.11upx;">
									<image style="width:100%;" src="/static/drawable-xhdpi/Property_80px_Yao.png" mode="widthFix"></image>
								</view>
							</view>
							<view class="restext" style="margin-top:9.72upx">
								擂台中输出<text style="color: #fb9605;">1.5</text>倍伤害
							</view>
							<view class="restext" style="margin-top:5.55upx">
								御灵团战、御灵试炼中受到<text style="color: #fb9605;">3</text>倍伤害
							</view>
						</view>
						<view class="beRestraintAttr">
							<view class="beRestrain">
								被克制
							</view>
							<view class="resimg">
								<view style="width:55.55upx;">
									<image style="width:100%;" src="/static/drawable-xhdpi/Property_80px_Mu.png" mode="widthFix"></image>
								</view>
								<view style="width:55.55upx; margin-left: 11.11upx;">
									<image style="width:100%;" src="/static/drawable-xhdpi/Property_80px_Lei.png" mode="widthFix"></image>
								</view>
							</view>
							<view class="restext" style="margin-top:9.72upx">
								擂台中输出<text style="color: #fb9605;">1.5</text>倍伤害
							</view>
							<view class="restext" style="margin-top:5.55upx">
								御灵团战、御灵试炼中受到<text style="color: #fb9605;">3</text>倍伤害
							</view>
						</view>
					</view>
					<view class="datatitle" style="position: relative; top:84.72upx">
						<view class="segmentation">
							<view class="leftcircle">
							</view>
							<view class="dashed"></view>
							<view class="rightcircle">
							</view>
						</view>
						<view class="retitle">
							技能详情
						</view>
					</view>
					<view class="skill">
						<view class="skillDetail">
							<view class="skillTop">
								<view class="choupi">
									臭屁
								</view>
								<view class="cdimg">
									<image style="width:100%; margin-top:-10.41upx" src="/static/drawable-xhdpi/ILLUSTRATION_consume_Icon.png" mode="widthFix"></image>
									<view style="color: #7feded; margin-left: 27.77upx; margin-top: -34.02upx;">2</view>
								</view>
								<view class="cd">
									CD:<text style="color: #7feded">2</text>秒
								</view>
							</view>
							<view class="skillBottom">
								臭不可闻！！！造成<text style="color: #ff6969">44%</text>的物理攻击力伤害
							</view>
						</view>
						<view class="skillDescription">升级详情</view>
						<view class="skillGrade">
							<view class="lv2">
								<text style="color:#93bad4;font-size: 23.61upx;margin-right:22.91upx">LV2</text>
								造成<text style="color:#ff6969">49%</text>的物理攻击力伤害
								<view class="xuxian"></view>
								<view class="yuan"></view>
							</view>
							<view class="lv3">
								<text style="color:#93bad4;font-size: 23.61upx;margin-right:22.91upx">LV3</text>
								造成<text style="color:#ff6969">55%</text>的物理攻击力伤害
								<view class="xuxian"></view>
								<view class="yuan"></view>
							</view>
							<view class="lv4">
								<text style="color:#93bad4;font-size: 23.61upx;margin-right:22.91upx">LV4</text>
								造成<text style="color:#ff6969">60%</text>的物理攻击力伤害
								<view class="xuxian"></view>
								<view class="yuan"></view>
							</view>
							<view class="lv5">
								<text style="color:#93bad4;font-size: 23.61upx;margin-right:22.91upx">LV5</text>
								造成<text style="color:#ff6969">66%</text>的物理攻击力伤害
							</view>
						</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		/* align-items: center;
		justify-content: center; */
		font-family: "Source Han Sans CN";
		background-size: contain;
	}
	.top {
		height:75.69upx;
		width: 100%;
		font-size: 41.66upx;
		text-align: center;
		color: #f2f2f2;
		background-image: url('/static/drawable-xhdpi/Back.png');
		background-repeat: no-repeat;
		background-position-x: 27.08upx;
		background-position-y: 6.94upx;
	}
	.detail {
		position: relative;
		width:100%;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.detailimg {
		width:513.88upx;
	}
	.left {
		position:absolute;
		top: 270.13upx;
		left: 26.38upx;
		width:28.47upx;
		height: 47.91upx;
	}
	.right {
		position: absolute;
		top: 270.13upx;
		right: 26.38upx;
		width: 28.47upx;
		height: 47.91upx;
	}
	.introduction {
		margin-top: 27.77upx;
	}
	.datatitle {
		display: flex;
		position: relative;
		align-items: center;
		justify-content: center;
	}
	.title {
		height: 34.02upx;
		width: 270.83upx;
		position: relative;
		z-index: 1;
		font-size:27.77upx;
		text-align: center;
		color:#fff;
		background-color: #93bad4;
		border-radius: 20.83upx;
	}
	.segmentation {
		xposition: relative;
	}
	.dashed {
		position: absolute;
		left:100upx;
		border-bottom: dashed 0.69upx #93bad4;
		width: 550upx;
		z-index: 1;
	}
	.leftcircle {
		position: absolute;
		width: 10.41upx;
		height:10.41upx;
		border-radius: 1000upx;
		background-color: #93bad4;
		left:100upx;
		top:12.5upx;
		z-index: 1;
	}
	.rightcircle {
		position: absolute;
		width: 10.41upx;
		height:10.41upx;
		border-radius: 1000upx;
		background-color: #93bad4;
		right:100upx;
		top:12.5upx;
		z-index: 1;
	}
	.grade {
		display: flex;
		flex-direction: row;
		padding: 51.38upx 61.11upx 0px 61.8upx;
		justify-content: space-between;
	}
	.circle {
		width:38.88upx;
		height: 38.88upx;
		border-radius: 69.44upx;
		background-color: #57b4fe;
	}
	.line {
		width: 431.25upx;
		height: 1.38upx;
		background-color: #999;
		position: relative;
		top: 19.44upx;
		left: -13.88upx;
	}
	.jishu {
		font-size: 19.44upx;
		text-align: center;
		color: #5aadfc;
	}
	.lowest {
		font-size: 26.38upx;
		text-align: center;
		color: #666;
	}
	.highest {
		font-size: 26.38upx;
		text-align: center;
		color: #666;
	}
	.parameter {
		display: flex;
		margin: 55.55upx 47.22upx 0px;
		width: 659.02upx;
		flex-direction: row;
		padding-top: 43.05upx;
		padding-left: 25upx;
		background-color: #f2f2e9;
		color: #666;
		border-radius: 13.88upx;
		box-sizing: border-box;
	}
	.picture {
		display: flex;
		width: 23.61upx;
		flex-direction: column;
		padding-top:5.55upx;
		padding-bottom: 42.36upx;
		justify-content: space-between;
	}
	.picture image {
		position:relative;
		width: 23.61upx;
	}
	.img1 {
		top: -6.94upx;
	}
	.img2 {
		top: -2.08upx;
	}
	.img4 {
		top:6.94upx;
	}
	.img5 {
		top: 9.02upx;
	}
	.description {
		font-size: 23.61upx;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		padding-top: 4.86upx;
		padding-bottom: 42.36upx;
	}
	.description view {
		position: relative;
		text-align: center;
		top: 4.86upx;
		left: 10.41upx;
	}
	.schedule {
		display: flex;
		flex-direction: column;
		padding-top: 8.33upx;
		padding-bottom: 48.61upx;
		justify-content: space-between;
		position:relative;
		left: 43.75upx;
	}
	.schedule view {
		position: relative;
		width:329.86upx;
	}
	.wugong {
		top: 9.02upx;
	}
	.wufang {
		top: 9.02upx;
	}
	.fagong {
		top: 6.94upx;
	}
	.fafang {
		top: 4.86upx;
	}
	.life {
		top: 3.47upx;
	}
	.digital {
		display: flex;
		flex-direction: column;
		padding-bottom: 42.36upx;
		justify-content: space-between;
		position:relative;
		left: 109.02upx;
		font-size: 29.16upx;
	}
	.digital view {
		position: relative;
	}
	.digital1 {
		top: 3.47upx;
	}
	.digital2 {
		top: 6.94upx;
	}
	.digital3 {
		top: 6.94upx;
	}
	.digital4 {
		top: 6.94upx;
	}
	.digital5 {
		top: 6.94upx;
	}
	.specific {
		position: relative;
	}
	.relationship {
		display: flex;
		flex-direction: column;
		font-size: 22.22upx;
		position:relative;
		margin: 101.38upx 47.22upx 0upx;
	}
	.restraintAttr {
		width: 659.02upx;
		height: 227.77upx;
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		background-color: #f2f2e9;
		border-radius: 13.88upx;
	}
	.restrain {
		width:74.3upx;
		height: 29.86upx;
		border-radius: 15.27upx;
		background-color: #2d7bc4;
		color: #fff;
		text-align: center;
		margin-top:23.61upx;
		margin-left: 33.33upx;
	}
	.resimg {
		display: flex;
		flex-direction: row;
		margin:18.75upx auto 0 65.97upx;	
	}
	.restext {
		margin-left: 65.97upx;
	}
	.beRestraintAttr {
		width: 659.02upx;
		height: 227.77upx;
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		background-color: #f2f2e9;
		border-radius: 13.88upx;
		margin-top:6.94upx;
	}
	.beRestrain {
		width:95.13upx;
		height: 29.86upx;
		border-radius: 15.27upx;
		background-color: #dc5c47;
		color: #fff;
		text-align: center;
		margin-top:23.61upx;
		margin-left: 29.16upx;
	}
	.retitle {
		height: 34.02upx;
		width: 159.72upx;
		position: relative;
		z-index: 2;
		font-size:27.77upx;
		text-align: center;
		color:#fff;
		background-color: #93bad4;
		border-radius: 20.83upx;
	}
	.skill {
		display: flex;
		flex-direction: column;
	}
	.skillDetail {
		width: 655.55upx;
		height: 162.5upx;
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		background-color: #f2f2e9;
		border-radius: 13.88upx;
		margin: 247.91upx 47.22upx 0upx;
	}
	.skillTop {
		display: flex;
		flex-direction: row;
		xjustify-content: space-between;
		width: 331.25upx;
	}
	.choupi {
		font-size: 29.16upx;
		color: #666;
	}
	.cd {
		font-size: 23.61upx;
		color: #666;
		position:relative;
		left: 163.19upx;
		top: 6.94upx;
	}
	.cdimg {
		font-size: 23.61upx;
		color: #666;
		position:relative;
		left: 98.61upx;
		top: 6.94upx;
		width:18.05upx;
		height:22.91upx;
		box-sizing: border-box;
		padding-top: 4.16upx;
	}
	.skillBottom {
		font-size: 18.05upx;
		color:#666;
	}
	.skillDescription {
		font-size: 29.16upx;
		color: #666;
		margin: 23.61upx auto 11.8upx 47.22upx;
	}
	.skillGrade {
		width: 654.86upx;
		height: 409.02upx;
		box-sizing: border-box;
		background-color: #f2f2e9;
		border-radius: 13.88upx;
		margin:0 47.22upx 43.05upx;
		font-size: 25upx;
		color: #666;
	}
	.lv2 {
		position: relative;
		top: 27.08upx;
		left: 33.33upx;
	}
	.lv3 {
		position: relative;
		top: 96.52upx;
		left: 33.33upx;
	}
	.lv4 {
		position: relative;
		top: 165.97upx;
		left: 33.33upx;
	}
	.lv5 {
		position: relative;
		top:235.41upx;
		left: 33.33upx;
	}
	.xuxian {
		position:absolute;
		height: 65.27upx;
		border-left: #93bad4 0.69upx dashed;
		left: 18.75upx;
	}
	.yuan {
		position: absolute;
		width:6.94upx;
		height: 6.94upx;
		border-box: box-sizing;
		background-color: #93bad4;
		border-radius: 694.44upx;
		left: 16.66upx;
		top: 97.22upx;
	}
</style>
