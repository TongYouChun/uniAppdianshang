<template>
	<view class="Data">
		<!-- 头像 -->
		<view class="HeadPortrait flex align-items space-between">
			<view class="TexT1 font-28 color-10">
				头像
			</view>
			<view class="TexT2 flex align-items">
				<image class="img" src="../../../static/backup_slices/My/Tx.png" mode=""></image>
				<image class="ing" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
		</view>
		
		<!-- 昵称 -->
		<view class="Li flex align-items space-between">
			<view class="TexT1 font-28 color-10">
				昵称
			</view>
			<view class="TexT2 font-28 color-3">
				未来
			</view>
		</view>
		
		<!-- 性别 -->
		<view class="Li flex align-items space-between">
			<view class="TexT1 font-28 color-10">
				性别
			</view>
			<view class="TexT2 font-28 color-3">
				女
			</view>
		</view>
	
		<!-- 我的手机号 -->
		<view class="Li flex align-items space-between">
			<view class="TexT1 font-28 color-10">
				我的手机号
			</view>
			<view class="TexT2 font-28 color-3">
				156****5850
			</view>
		</view>
	
		<!-- 我的二维码 -->
		<view class="Li flex align-items space-between">
			<view class="TexT1 font-28 color-10">
				我的二维码
			</view>
			<view class="TexT2 font-28 color-3">
				<image class="ing" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
		</view>
			
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.Data{
		.HeadPortrait{
			padding: 0 30upx 0 28upx;
			height: 150upx;
			border-bottom: 1upx solid #f5f5f5;
			.TexT2{
				height: 150upx;
				.img{
					margin-right: 42upx;
					height: 100upx;
					width: 100upx;
					border: 1upx solid #f5f5f5;
					border-radius: 50%;
				}
				.ing{
					height: 26upx;
					width: 15upx;
				}
			}
		}
		.Li{
			padding: 0 30upx 0 28upx;
			height: 78upx;
			border-bottom: 1upx solid #f5f5f5;
			.TexT2{
				.ing{
					height: 26upx;
					width: 15upx;
				}
			}
		}
	}
</style>
