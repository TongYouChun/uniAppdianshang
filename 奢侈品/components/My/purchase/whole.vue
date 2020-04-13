<template>
	<!-- 全部产品 -->
	<view class="purchase flex-column height">
		<view class="product flex-column background-f" v-for="(item,index) in Commoditya" :key="index">
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
	
</template>

<script>
	export default {
		props:{
			Commoditya: ''
		},
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	// 全部 产品
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

</style>
