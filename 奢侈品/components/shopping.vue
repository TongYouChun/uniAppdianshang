<template>
	<view class="Content flex-column">
		<!-- 购物商品 -->
		<view class="shopping flex-column background-f" v-for="(item,index) in commodityTexT" :key="index">
			<!-- 购物商品名称 -->
			<view class="h4 flex align-items">
				<image class="Ig" :src="item.Ig" mode=""></image>
				<image class="ing" :src="item.ing" mode=""></image>
				<text class="font-26 color-3">{{item.name}}</text>
				<image class="In" src="../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<!-- 购物商品信息 -->
			<view class="Name flex">
				<view class="Ig flex align-items">
					<image class="ig" :src="item.Ig" mode=""></image>
				</view>
				<view class="Itg">
					<image class="itg" :src="item.itg" mode=""></image>
				</view>
				<view class="TeVT flex-column">
					<text class="tet font-26 color-3">{{item.introduce}}</text>
					<view class="VexT flex align-items justify-content">
						<text class="font-30 color-6">{{item.Model}}</text>
						<image class="ng" src="../../static/backup_slices/mipmap-xxhdpi/xia.png" mode=""></image>
					</view>
					<!-- 钱 -->
					<view class="money flex space-between align-items">
						<text class="TeT font-32 color-3 font-600">¥ {{item.cash}}</text>
						<view class="TexT flex">
							<view class="Text">
								<text></text>
							</view>
							<view class="texT flex align-items justify-content">
								{{item.Number}}
							</view>
							<view class="Text">
								<text></text>
								<view class="text"></view>
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
		props:{
			commodityTexT: ''
		},
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.Content{
		.shopping{
			margin-bottom: 40upx;
			width: 674upx;
			height: 405upx;
			border-radius: 14upx;
			padding-left: 26upx;
			.h4{
				height: 134upx;
				.Ig{
					height: 34upx;
					width: 34upx;
					border: 3upx solid #f5f5f5;
					border-radius: 50%;
				}
				.ing{
					margin: 0 12upx 0 22upx;
					width: 39upx;
					height: 36upx;
				}
				text{
					height: 26upx;
					line-height: 26upx;
				}
				.In{
					margin-left: 22upx;
					width: 12upx;
					height: 20upx;
				}
			}
			// 购物商品信息
			.Name{
				flex: 1;
				.Ig{
					height: 179upx;
					.ig{
						height: 34upx;
						width: 34upx;
						border: 3upx solid #f5f5f5;
						border-radius: 50%;
					}
				}
				.Itg{
					margin: 0 28upx 0 30upx;
					height: 100%;
					.itg{
						height: 179upx;
						width: 179upx;
					}
				}
				.TeVT{
					flex: 1;
					align-items: flex-start;
					.tet{
						width: 375upx;
						line-height: 30upx;
					}
					.VexT{
						margin: 30upx 0;
						padding: 0 10upx;
						height: 50upx;
						background: #F9F9F9;
						text{
							height: 30upx;
							line-height: 30upx;
						}
						.ng{
							height: 30upx;
							width: 30upx;
						}
					}
					.money{
						width: 100%;
						.TeT{
							height: 26upx;
							line-height: 26upx;
						}
						.TexT{
							margin-right: 34upx;
							.Text{
								position: relative;
								height: 45upx;
								width: 50upx;
								border: 1upx solid #CCCCCC;
								text{
									position: absolute;
									top: 0;
									left: 0;
									bottom: 0;
									right: 0;
									margin: auto;
									width: 28upx;
									height: 3upx;
									background: #333;
								}
								.text{
									position: absolute;
									top: 0;
									left: 0;
									bottom: 0;
									right: 0;
									margin: auto;
									margin: auto;
									width: 3upx;
									height: 28upx;
									background: #333;
								}
							}
							.texT{
								height: 45upx;
								width: 80upx;
								border: 1upx solid #CCCCCC;
							}
						}
					}
				}
			}
		}
	}
</style>
