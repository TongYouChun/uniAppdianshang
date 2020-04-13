<template>
	<view class="Package flex-column height">
		<!-- 轮播图 -->
		<view class="RotationChart">
			腕表
		</view>
		<view class="container flex-column">
			<view class="h4 flex justify-content align-items">
				<text></text>
				<text class="font-30">精选推荐</text>
				<text></text>
			</view>
			<view class="product flex">
				<view class="li flex-column align-items" v-for="(item,index) in information" :key="index">
					<image class="img" src="" mode=""></image>
					<text class="font-20">{{item}}</text>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				information: ['Tiffany','APM','Swaroski','Pandora','Gucci','仙蒂瑞拉','佐卡伊','古钻','Clovis','Magifas','Daisy Fellowes','SUEMOMO']
			};
		}
	}
</script>

<style lang="scss">
	.Package{
		.RotationChart{
			height: 200upx;
			width: 570upx;
			background: #4CD964;
		}
		.container{
			flex: 1;
			.h4{
				height: 110upx;
				width: 100%;
				text:nth-child(1),text:nth-child(3){
					width: 100upx;
					height: 2upx;
					background: #101010;
				}
				text:nth-child(2){
					margin: 0 14upx;
					height: 30upx;
					line-height: 30upx;
					color: #101010;
				}
			}
			.product{
				flex-wrap: wrap;
				flex: 1;
				.li{
					margin: 0 25upx;
					width: 150upx;
					.img{
						width: 120upx;
						height: 120upx;
						background: #007AFF;
					}
					text{
						height: 20upx;
						line-height: 20upx;
						margin: 15upx 0 47upx 0;
						color: #101010;
					}
				}
			}
		}
	}
</style>

<style>

</style>
