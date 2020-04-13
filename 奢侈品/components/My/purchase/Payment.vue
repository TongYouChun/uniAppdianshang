<template>
	<view class="Payment flex-column height" >
		
		<view class="payment flex-column" v-for="(item,index) in Commodity" :key="index">
			<view class="Product flex-column">
				<view class="product flex-column background-f">
					<!-- 产品名称 -->
					<view class="product-top flex space-between">
						<view class="Name-left flex align-items">
							<image class="ing" :src="item.ing" mode=""></image>
							<text class="font-24 color-6">{{item.Name1}}</text>
							<image class="ig" :src="item.ig" mode=""></image>
						</view>
						<view class="Name-right font-24">
							{{item.Name2}}
						</view>
					</view>
					<!-- 内容 -->
					<view class="product-Middle flex-column">
						<view class="Content flex space-between">
							<view class="Content-left">
								<image class="mg" :src="item.mg" mode=""></image>
							</view>
							<view class="Content-right flex-column space-between">
								<text class="text font-28 color-10">{{item.TexT}}</text>
								<view class="TexT font-24 color-6 flex">
									<text >尺码:</text>
									<text>{{item.TecT}}</text>
								</view>
							</view>
						</view>
						<view class="money flex space-between">
							<view class="money-left font-28 color-6">
								<text>{{item.text}}</text>
							</view>
							<view class="money-right font-28 color-6">
								<text>价格：</text>
								<text>$</text>
								<text>{{item.tect}}</text>
							</view>
						</view>
					</view>
					<!-- 付款 -->
					<view class="product-bottom flex space-around">
						<view class="li font-28 color-3">
							{{item.payment1}}
						</view>
						<view class="li font-28 color-3">
							{{item.payment2}}
						</view>
						<view class="li font-28 color-3">
							{{item.payment3}}
						</view>
					</view>
				</view>
			</view>
			<!-- 猜你喜欢 -->
			<view class="Like flex-column align-items">
				<!-- 猜你喜欢 -->
				<view class="h4 flex">
					<view class="Ig">
						<image class="ig" src="../../../static/backup_slices/My/zan1.png" mode=""></image>
					</view>
					<text class="font-30">猜你喜欢</text>
				</view>
				<view class="like flex space-around">
					<view class="commodity flex-column" v-for="(itm,inx) in item.like" :key="inx">
						<image class="ing" :src="itm.Ig" mode=""></image>
						<text class="text font-26 color-10">{{itm.tex}}</text>
						<view class="TexT flex space-between align-items">
							<text class="font-24 color-10">{{itm.TexT1}}</text>
							<text class="font-24">{{itm.TexT2}}</text>
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
			Commodity: ''
		},
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

<style lang="scss">
	.Payment{
		.Product{
			.product{
				margin-bottom: 48upx;
				width: 710upx;
				height: 515upx;
				.product-top{
					height: 84upx;
					line-height: 84upx;
					.Name-left{
						margin-left: 25upx;
						.ing{
							height: 30upx;
							width: 30upx;
						}
						text{
							margin: 0 20upx 0 10upx;
						}
						.ig{
							height: 24upx;
							width: 14upx;
						}
					}
					.Name-right{
						margin-right: 30upx;
						color: #F78D00;
					}
				}
				.product-Middle{
					.Content{
						margin: 0 30upx 0 25upx;
						.Content-left{
							.mg{
								width: 208upx;
								height: 192upx;
								border: 1upx solid #f5f5f5;
							}
						}
						.Content-right{
							margin-left: 18upx;
							
							.text{
								line-height: 34upx;
							}
							.TexT{
								margin-bottom: 15upx;
								height: 24upx;
								line-height: 24upx;
								text:nth-child(2){
									margin-left: 10upx;
								}
							}
						}
					}
					.money{
						margin: 20upx 35upx 100upx 130upx;
						line-height: 28upx;
					}
				}
				.product-bottom{
					margin-left: 100upx;
					.li{
						padding: 0 20upx;
						height: 50upx;
						line-height: 50upx;
						border: 2upx solid #666;
						border-radius: 14upx;
					}
					.li:last-child{
						border: 2upx solid #FFA732;
						color: #FFA732;
					}
				}
			}
		}
		.Like{
			width: 750upx;
			.h4{
				.Ig{
					width: 36upx;
					height: 36upx;
					background: #FFA732;
					border-radius: 50%;
					.ig{
						height: 36upx;
						width: 36upx;
						border-radius: 50%;
					}
				}
				text{
					margin-left: 16upx;
					color: #FFA732;
				}
			}
			.like{
				flex-wrap: wrap;
				margin-top: 25upx;
				width: 750upx;
				.commodity{
					height: 490upx;
					width: 282upx;
					.ing{
						height: 320upx;
						width: 282upx;
					}
					.text{
						line-height: 32upx;
					}
					.TexT{
						margin-top: 20upx;
						text:nth-child(1){
							
						}
						text:nth-child(2){
							padding: 12upx;
							color: #FFA732;
							border: 2upx solid #FFA732;
							border-radius: 14upx;
						}
					}
				}
			}
		}
	}
	
</style>
