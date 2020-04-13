<template>
	<view class="Curing flex-column">
		<view class="curing flex background-f" v-for="(item,index) in ContentTexT" :key="index">
			<image class="ing" :src="item.ing" mode=""></image>
			<view class="information flex-column">
				<view class="TexT1 font-28 color-3">
					{{item.TexT1}}
				</view>
				<view class="TexT2 font-22 color-3">
					{{item.TexT2}}
				</view>
				<view class="TexT3 flex space-between">
					<text class="font-28 color-3">$ {{item.qian}}</text>
					<text class="font-24 color-f">{{item.text}}</text>
				</view>
				<view class="TexT4 flex">
					<view class="li flex align-items" v-for="(itm,iex) in item.Li" :key="iex">
						<image class="ig" :src="itm.ig" mode=""></image>
						<text class="font-16 color-10">{{itm.text}}</text>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props:{
			ContentTexT:''
		},
		data() {
			return {
				
			}
		}
	}
</script>

<style lang="scss">
	.Curing{
		.curing{
			margin-bottom: 46upx;
			padding: 36upx 0 30upx 20upx;
			width: 100%;
			.ing{
				height: 240upx;
				width: 220upx;
			}
			.information{
				flex: 1;
				.TexT1{
					margin: 24upx 0 0 28upx;
					height: 28upx;
					line-height: 28upx;
				}
				.TexT2{
					margin: 30upx 0 0 28upx;
					height: 22upx;
					line-height: 22upx;
				}
				.TexT3{
					margin: 42upx 34upx 0 44upx;
					text:nth-child(1){
						height: 54upx;
						line-height: 54upx;
					}
					text:nth-child(2){
						height: 54upx;
						line-height: 54upx;
						text-align: center;
						width: 160upx;
						background: #000;
						border-radius: 16upx;
					}
				}
				.TexT4{
					justify-content: flex-end;
					margin-right: 24upx;
					margin-top: 60upx;
					height: 30upx;
					.li{
						.ig{
							width: 30upx;
							height: 30upx;
						}
						text{
							width: 70upx;
						}
					}
				}
			}
		}
	}
</style>
