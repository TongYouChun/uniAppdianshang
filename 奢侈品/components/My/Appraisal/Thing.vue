<template>
	<view class="Thing flex-column">
		<view class="thing background-f">
			<view class="Name flex">
				<image class="nig" src="../../../static/backup_slices/My/Tx.png" mode=""></image>
				<view class="TexT flex-column">
					<text class="font-32 color-10">未来</text>
					<text class="font-24 color-3">6-23 18:00</text>
				</view>
			</view>
			<view class="Img flex">
				<image class="ig" src="../../../static/backup_slices/My/x1.1.png" mode=""></image>
				<image class="ig" src="../../../static/backup_slices/My/x1.2.png" mode=""></image>
				<image class="ig" src="../../../static/backup_slices/My/x1.3.png" mode=""></image>
			</view>
			<view class="appraisal flex justify-content">
				<text class="font-28 color-10">正在鉴定中</text>
			</view>
		</view>
	</view>
</template>

<script>
</script>

<style lang="scss">
	.Thing{
		.thing{
			width: 690upx;
			.Name{
				margin: 16upx 0 0 50upx;
				height: 120upx;
				.nig{
					height: 100upx;
					width: 100upx;
				}
				.TexT{
					margin-left: 16upx;
					text:nth-child(1){
						margin-top: 16upx;
						height: 32upx;
						line-height: 32upx;
					}
					text:nth-child(2){
						margin-top: 24upx;
						height: 20upx;
						line-height: 20upx;
					}
				}
			}
			.Img{
				flex-wrap: wrap;
				margin-left: 40upx;
				.ig{
					height: 218upx;
					width: 206upx;
				}
			}
			.appraisal{
				height: 94upx;
				text{
					margin-top: 22upx;
					height: 28upx;
				}
			}
		}
	}
</style>
