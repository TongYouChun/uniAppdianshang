<template>
	<view class="Zhaohuo flex-column">
		<!-- 搜索 -->
		<view class="Search flex align-items justify-content">
			<view class="search flex align-items">
				<input class="input font-28" type="text" value="" placeholder="女包"/>
				<image class="img" src="../../../static/backup_slices/My/X.png" mode=""></image>
			</view>
			<text class="Button font-28">搜索</text>
		</view>
		<!-- 商品 -->
		<view class="Commodity flex-column">
			<view class="commodity flex">
				<image class="Img" src="../../../static/backup_slices/My/coco.png" mode=""></image>
				<view class="TexT flex-column space-between">
					<view class="Text flex-column ">
						<text class="font-32 color-10">Ferrgt 手提包</text>
						<view class="text font-24 color-3 flex-column">
							<text>98新迈克高仕红色牛皮女士</text>
							<text>手提包</text>
						</view>
					</view>
					<view class="texT flex space-between space-between align-items">
						<text class="font-28 color-3">$ 200-300</text>
						<text class="font-28">咨询订购</text>
					</view>
				</view>
			</view>
			<view class="commodity flex">
				<image class="Img" src="../../../static/backup_slices/My/coco.png" mode=""></image>
				<view class="TexT flex-column space-between">
					<view class="Text flex-column ">
						<text class="font-32 color-10">Ferrgt 手提包</text>
						<view class="text font-24 color-3 flex-column">
							<text>98新迈克高仕红色牛皮女士</text>
							<text>手提包</text>
						</view>
					</view>
					<view class="texT flex space-between space-between align-items">
						<text class="font-28 color-3">$ 200-300</text>
						<text class="font-28">咨询订购</text>
					</view>
				</view>
			</view>
			<view class="commodity flex">
				<image class="Img" src="../../../static/backup_slices/My/coco.png" mode=""></image>
				<view class="TexT flex-column space-between">
					<view class="Text flex-column ">
						<text class="font-32 color-10">Ferrgt 手提包</text>
						<view class="text font-24 color-3 flex-column">
							<text>98新迈克高仕红色牛皮女士</text>
							<text>手提包</text>
						</view>
					</view>
					<view class="texT flex space-between space-between align-items">
						<text class="font-28 color-3">$ 200-300</text>
						<text class="font-28">咨询订购</text>
					</view>
				</view>
			</view>
			<view class="commodity flex">
				<image class="Img" src="../../../static/backup_slices/My/coco.png" mode=""></image>
				<view class="TexT flex-column space-between">
					<view class="Text flex-column ">
						<text class="font-32 color-10">Ferrgt 手提包</text>
						<view class="text font-24 color-3 flex-column">
							<text>98新迈克高仕红色牛皮女士</text>
							<text>手提包</text>
						</view>
					</view>
					<view class="texT flex space-between space-between align-items">
						<text class="font-28 color-3">$ 200-300</text>
						<text class="font-28">咨询订购</text>
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
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.Zhaohuo{
		// 搜索
		.Search{
			margin-top: 45upx;
			width: 750upx;
			.search{
				width: 546upx;
				height: 76upx;
				border: 2upx solid #C9C9C9;
				border-radius: 38upx;
				.input{
					width: 420upx;
					margin: 0 25upx 0 35upx;
					height: 76upx;
				}
				.img{
					height: 34upx;
					width: 34upx;
				}
			}
			.Button{
				margin-left: 30upx;
				color: #FD9226;
			}
		}
		// 商品
		.Commodity{
			.commodity{
				margin-top: 18upx;
				.Img{
					margin-left: 30upx;
					height: 258upx;
					width: 236upx;
				}
				.TexT{
					flex: 1;
					margin: 0 50upx 0 14upx;
					.Text{
						.text{
							line-height: 50upx;
						}
					}
					.texT{
						text:nth-child(2){
							padding: 12upx 24upx;
							color: #FD9226;
							border: 2upx solid #FD9226;
							border-radius: 13upx;
						}
					}
				}
			}
		}
	}
</style>
