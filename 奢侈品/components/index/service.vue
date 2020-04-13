<template>
	<view class="Service flex-column align-items">
		<!-- 背景图 -->
		<view class="chart flex-column">
			<image class="Img" src="../../static/backup_slices/mipmap-xxhdpi/banner1.png" mode=""></image>
			<text class="font-20 color-f">OCCUPATIONAL SKILL TESTING AUTHORITY</text>
			<text class="font-28 color-f">专业 信赖 专注</text>
		</view>
		<view class="service flex-column width-710 background-f" v-for="(item,index) in ContentTexT" :key="index">
			<!-- 头 图片 -->
			<view class="service-top flex space-between">
				<view class="TET flex">
					<image class="ing" :src="item.ing" mode=""></image>
					<view class="TexT flex-column">
						<text class="font-36 color-3">{{item.Name}}</text>
						<text class="font-24 color-9">{{item.shijian}}</text>
					</view>
				</view>
				
				<view class="Img flex">
					<view class="text1 flex-column">
						<image class="ing" :src="item.cakan" mode=""></image>
						<text class="font-16 color-3">{{item.cakantext}}</text>
					</view>
					<view class="text2 flex-column">
						<image class="ing" :src="item.xingxi" mode=""></image>
						<text class="font-16 color-3">{{item.xingxitext}}</text>
					</view>
				</view>
			
			</view>
			<!-- 信息 图片 -->
			<view class="service-Middle flex-column">
				<view class="text font-28 color-3">
					{{item.TexT}}
				</view>
				<view class="Ing flex">
					<view class="texT flex" v-for="(iem,inx) in item.Ig" :key="inx">
						<image class="ing" :src="iem" mode=""></image>
					</view>
				</view>
			</view>
			<!-- 名称 图片 -->
			<view class="service-bottom flex">
				<view class="Ig">
					<image class="ig" :src="item.ig" mode=""></image>
					<view class="text font-16 color-f">{{item.text}}</view>
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
	.Service{
		// 背景图
		.chart{
			position: relative;
			z-index: 0;
			width: 100%;
			height: 240upx;
			.Img{
				position: absolute;
				z-index: -1;
				top: 0;
				left: 0;
				width: 100%;
				height: 240upx;
			}
			text:nth-child(2){
				margin: 68upx 0 0 26upx;
				height: 15upx;
				line-height: 15upx;
			}
			text:nth-child(3){
				margin: 38upx 0 0 92upx;
				height: 28upx;
				line-height: 28upx;
			}
		}
		// 鉴定内容
		.service{
			margin-top: 54upx;
			.service-top{
				.TET{
					margin: 20upx 0 0 62upx;
					.ing{
						height: 100upx;
						width: 100upx;
					}
					.TexT{
						margin: 20upx 0 0 10upx;
						text:nth-child(1){
							height: 36upx;
							line-height: 36upx;
						}
						text:nth-child(2){
							margin-top: 12upx;
							height: 20upx;
							line-height: 20upx;
						}
					}
				}
				.Img{
					margin: 55upx 87upx 0 0;
					.text1{
						.ing{
							margin-bottom: 5upx;
							width: 37upx;
							height: 23upx;
						}
					}
					.text2{
						margin-left: 18upx;
						.ing{
							width: 33upx;
							height: 27upx;
						}
					}
				}
			}
			.service-Middle{
				.text{
					margin: 35upx 116upx 18upx 72upx;
					line-height: 40upx;
				}
				.Ing{
					margin-left: 70upx;
					flex-wrap: wrap;
					.ing{
						margin: 3upx;
						height: 200upx;
						width: 188upx;
					}
				}
			}
			.service-bottom{
				height: 88upx;
				position: relative;
				.Ig{
					position: absolute;
					z-index: 0;
					bottom: 18upx;
					right: 0;
					height: 51upx;
					width: 51upx;
					.ig{
						height: 51upx;
						width: 51upx;
					}
					.text{
						position: absolute;
						top: 0;
						left: 0;
						width: 51upx;
						height: 51upx;
						line-height: 51upx;
						text-align: center;
					}
				}
			}
		}
	}
</style>
