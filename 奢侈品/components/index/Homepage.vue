<template>
	<view class="Homepage flex-column align-items">
		<!-- 轮播图 -->
		<view class="chart">
			<view class="page-section swiper">
				<view class="page-section-spacing">
					<swiper class="swiper" indicator-dots="true" circular="true" indicator-active-color="#fff" autoplay="true" interval="2000" duration="500">
						<swiper-item>
							<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner11.png" mode=""></image>
						</swiper-item>
						<swiper-item>
							<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner22.png" mode=""></image>
						</swiper-item>
						<swiper-item>
							<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner33.png" mode=""></image>
						</swiper-item>
						<swiper-item>
							<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner44.png" mode=""></image>
						</swiper-item>
					</swiper>
				</view>
			</view>
		</view>
		<!-- 选项 -->
		<view class="option flex width-710 background-f align-items">
			<view class="li flex" @click="Appraisal()">
				<text class="font-28">鉴定</text>
				<image class="ing" src="../../static/backup_slices/mipmap-xxhdpi/heixian.png" mode=""></image>
			</view>
			<view class="li flex" @click="curing()">
				<text class="font-28">养护</text>
				<image class="ing" src="../../static/backup_slices/mipmap-xxhdpi/heixian.png" mode=""></image>
			</view>
			<view class="li flex">
				<text class="font-28">求购</text>
				<image class="ing" src="../../static/backup_slices/mipmap-xxhdpi/heixian.png" mode=""></image>
			</view>
			<view class="li flex">
				<text class="font-28">商城</text>
			</view>
		</view>
		<!-- 产品 -->
		<view class="product flex background-f justify-content">
			<view class="li flex-column align-items">
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/ozho.png" mode=""></image>
				<text class="font-28">欧洲尖货</text>
			</view>
			<view class="li flex-column align-items">
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/jingxuan.png" mode=""></image>
				<text class="font-28">买手精选</text>
			</view>
		</view>
		<!-- 轻奢品牌 -->
		<view class="brand flex-column background-f">
			<view class="h5 flex space-between align-items">
				<text class="font-34">轻奢品牌</text>
				<image class="ing" src="../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<view class="Img flex justify-content">
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner5.png" mode=""></image>
			</view>
		</view>
		<!-- 猜你喜欢 -->
		<view class="like flex-column background-f">
			<view class="h5 flex space-between align-items">
				<text class="font-34">猜你喜欢</text>
				<image class="ing" src="../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<view class="Img flex">
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner11.png" mode=""></image>
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner44.png" mode=""></image>
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner33.png" mode=""></image>
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/banner22.png" mode=""></image>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		},
		methods:{
			Appraisal() {
				uni.navigateTo({
					url:'/pages/index/Appraisal'
				})
			},
			curing () {
				uni.navigateTo({
					url:'/pages/index/Curing'
				})
			}
		}
	}
</script>

<style lang="scss">
	.Homepage{
		width: 100%;
		// 轮播图
		.chart{
			width: 100%;
			height: 292upx;
			.swiper{
				width: 100%;
				height: 292upx;
				.img{
					width: 100%;
					height: 292upx;
				}
			}
		}
		// 选项
		.option{
			margin: 44upx 0;
			height: 108upx;
			.li{
				flex: 1;
				text{
					margin: 0 62upx 0 56upx;
					height: 28upx;
					line-height: 28upx;
					color: #101010;
				}
				.ing{
					width: 1upx;
					height: 24upx;
				}
			}
		}
		// 产品
		.product{
			width: 100%;
			height: 326upx;
			.li{
				margin-top: 28upx;
				margin-right: 6upx;
				.img{
					width: 352upx;
					height: 240upx;
				}
				text{
					margin-top: 16upx;
					height: 28upx;
					line-height: 28upx;
				}
			}
		}
		// 轻奢品牌
		.brand{
			margin: 57upx 0 54upx 0;
			width: 100%;
			height: 396upx;
			.h5{
				height: 86upx;
				margin: 0 44upx 0 20upx;
				text{
					height: 34upx;
					line-height: 34upx;
					color: #101010;
				}
				.ing{
					width: 12upx;
					height: 24upx;
				}
			}
			.Img{
				width: 100%;
				height: 310upx;
				.img{
					width: 710upx;
					height: 280upx;
				}
			}
		}
		// 猜你喜欢
		.like{
			margin-bottom: 44upx;
			width: 100%;
			height: 360upx;
			.h5{
				height: 82upx;
				margin: 0 44upx 0 20upx;
				text{
					height: 34upx;
					line-height: 34upx;
					color: #101010;
				}
				.ing{
					width: 12upx;
					height: 24upx;
				}
			}
			.Img{
				padding: 0 20upx;
				height: 310upx;
				overflow-x: auto;
				.img{
					flex: 0 0 300upx;
					margin-right: 12upx;
					height: 240upx;
					border: 1upx solid #F5F5F5;
					border-radius: 10upx;
				}
			}
		}
	}
</style>
