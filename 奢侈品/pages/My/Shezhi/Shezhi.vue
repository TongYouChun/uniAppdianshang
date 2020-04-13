<template>
	<!-- 设置 -->
	<view class="Shezhi flex-column height">
		<!-- 个人信息 收货地址 申请认证 -->
		<view class="personal">
			<!-- 个人信息 -->
			<view class="Li flex space-between align-items" @click="information()">
				<text class="font-28 color-10">个人信息</text>
				<image class="img" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<!-- 收货地址 -->
			<view class="Li flex space-between align-items">
				<text class="font-28 color-10">收货地址</text>
				<image class="img" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<!-- 申请认证 -->
			<view class="Li flex space-between align-items">
				<text class="font-28 color-10">申请认证</text>
				<image class="img" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
		</view>
		<!-- 消息提醒 清除缓存 帮助中心 奢侈二手交易用户协议 关于奢侈二手交易(V3.7.1） -->
		<view class="news">
			<view class="Li flex space-between align-items">
				<text class="font-28 color-10">消息提醒</text>
				<view class="Button flex-column start" :class="Te" @click="Chang">
					<view class="text"></view>
				</view>
			</view>
			<view class="Li flex space-between align-items">
				<text class="font-28 color-10"> 清除缓存</text>
				<image class="img" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<view class="Li flex space-between align-items">
				<text class="font-28 color-10">帮助中心</text>
				<image class="img" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<view class="Li flex space-between align-items">
				<text class="font-28 color-10">奢侈二手交易用户协议</text>
				<image class="img" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
			<view class="Li flex space-between align-items">
				<text class="font-28 color-10">关于奢侈二手交易(V3.7.1</text>
				<image class="img" src="../../../static/backup_slices/mipmap-xxhdpi/you1.png" mode=""></image>
			</view>
		</view>
		<!-- 退出登录 -->
		<view class="tuichu">
			<button class="button" type="primary">退出登录</button>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				// 消息提醒
				Te: '',
				chang: false
			};
		},
		methods:{
			// 个人信息
			information () {
				uni.navigateTo({
					url:'/pages/My/Data/Data'
				})
			},
			// 消息提醒
			Chang () {
				if(this.chang) {
					this.Te = 'te';
					this.chang = false
				} else {
					this.Te = '';
					this.chang= true
				}
			}
		}
	}
</script>

<style lang="scss">
	// 设置 
	.Shezhi{
		position: relative;
		// 个人信息 收货地址 申请认证
		.personal{
			height: 304upx;
			.Li{
				padding: 0 40upx 0 26upx;
				height: 102upx;
				border-bottom: 1upx solid #F5F5F5;
				.img{
					width: 15upx;
					height: 25upx;
				}
			}
		}
		// 消息提醒 清除缓存 帮助中心 奢侈二手交易用户协议 关于奢侈二手交易(V3.7.1）
		.news{
			border-top: 32upx solid #f5f5f5;
			.Li{
				padding: 0 40upx 0 26upx;
				height: 102upx;
				border-bottom: 1upx solid #F5F5F5;
				.img{
					width: 15upx;
					height: 25upx;
				}
				.Button{
					height: 36upx;
					width: 60upx;
					border-radius: 18upx;
					border: 1upx solid #f5f5f5;
					// background: #FD9226;
					.text{
						margin: 1upx;
						height: 31upx;
						width: 31upx;
						border-radius: 50%;
						border: 1upx solid #f5f5f5;
						background: #FFFFFF;
					}
				}
				.te{
					align-items: flex-end;
					background: #FD9226;
				}
			}
		}
		.tuichu{
			position: absolute;
			z-index: 0;
			left: 0;
			bottom: 0;
			width: 750upx;
			height: 98upx;
			.button{
				height: 98upx;
				line-height: 98upx;
				border-radius: 0;
				background: #FD9226;
				font-size: 36upx;
			}
		}
	}
</style>
