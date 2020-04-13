<template>
	<view class="Shopping height flex-column align-items">
		<!-- 产品信息 -->
		<view class="Shopping-content flex-column flex-overflow">
			<shopping :commodityTexT = 'commodityTexT'></shopping>
		</view>
		<!-- 产品钱 -->
		<view class="Money flex space-between background-f">
			<view class="Choice flex align-items space-between">
				<view class="TexT1 flex">
					<image class="Ig" src="" mode=""></image>
					<text class="font-26 color-3">全选</text>
				</view>
				<view class="TexT2 font-36 color-3 font-600">
					¥2927
				</view>
			</view>
			<view class="payment flex align-items justify-content font-30 color-f">
				结算（2）
			</view>
		</view>
	</view>
</template>

<script>
	import shopping  from '../../components/shopping.vue'
	export default {
		data() {
			return {
				commodityTexT: [
					{
						Ig: '../../static/backup_slices/mipmap-xxhdpi/xuanze.png',
						ing: '../../static/backup_slices/My/shop-selected.png',
						name:'Tiffany & Co.',
						itg:'../../static/backup_slices/mipmap-xxhdpi/2.png',
						introduce: 'Keys系列925纯银心形钥匙迷你 吊坠项链 GRP02635',
						Model:'银色-16英寸',
						cash:'2848',
						Number: 1
					},{
						Ig: '../../static/backup_slices/mipmap-xxhdpi/xuanze.png',
						ing: '../../static/backup_slices/My/shop-selected.png',
						name:'Whittard',
						itg:'../../static/backup_slices/mipmap-xxhdpi/2.1.png',
						introduce: '爱丽丝梦游仙境马克杯（爱丽丝） 267039',
						Model:'白色',
						cash:'79',
						Number: 1
					}
				]
			}
		},
		components: {
			shopping
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.Shopping{
		background: #f5f5f5;
		.Shopping-content{
		}
		.Money{
			position: fixed;
			bottom: 0;
			left: 0;
			width: 100%;
			height: 110upx;
			.Choice{
				flex: 1;
				.TexT1{
					.Ig{
						margin: 0 30upx 0 50upx;
						height: 34upx;
						width: 34upx;
						border: 3upx solid #ddd;
						border-radius: 50%;
					}
				}
				.TexT2{
					margin-right: 32upx;
					height: 36upx;
					line-height: 36upx;
				}
			}
			.payment{
				width: 260upx;
				background: #464646;
			}
		}
	}
</style>
