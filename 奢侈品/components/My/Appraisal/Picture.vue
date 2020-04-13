<template>
	<view class="Picture flex-column">
		<!-- 图片鉴定 -->
		<view class="commodity background-f">
			<view class="h4 flex">
				<text class="tex font-28 color-10">LV海外旗舰店</text>
				<image class="img" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<view class="TexT font-24">
				Louis Vuitton/路易威登 女士咖啡色拼红色皮革LOGO印花 皮质单肩斜挎包手提包
			</view>
			<view class="Img flex">
				<image class="ing" src="../../../static/backup_slices/My/1.1.png" mode=""></image>
				<image class="ing" src="../../../static/backup_slices/My/1.2.png" mode=""></image>
				<image class="ing" src="../../../static/backup_slices/My/1.3.png" mode=""></image>
			</view>
			<view class="TecT flex justify-content">
				<text class="font-28 color-3">正在鉴定中</text>
			</view>
		</view>
	</view>
</template>

<script>
</script>

<style lang="scss">
	.Picture{
		.commodity{
			margin-bottom: 60upx;
			width: 700upx;
			.h4{
				margin: 40upx 0 20upx 0;
				.tex{
					margin: 0 28upx 0 48upx;
					height: 28upx;
					line-height: 28upx;
				}
				.img{
					width: 14upx;
					height: 24upx;
				}
			}
			.TexT{
				margin: 0 40upx 0 45upx;
				color: #101010;
			}
			.Img{
				flex-wrap: wrap;
				margin: 10upx 40upx 0 45upx;
				.ing{
					height: 218upx;
					width: 206upx;
				}
			}
			.TecT{
				margin: 20upx 0 40upx 0;
				width: 100%;
			}
		}
	}
</style>
