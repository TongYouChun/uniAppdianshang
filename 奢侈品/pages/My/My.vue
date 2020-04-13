<template>
	<view class="My flex-column height">
		<!-- 头像设置 -->
		<view class="Head">
			
			<!-- 设置 -->
			<view class="SetUp flex align-items">
				<!-- 信息 -->
				<image class="iag" src="../../static/backup_slices/My/information.png" mode="" ></image>
				<!-- 设置 -->
				<image class="ibg" src="../../static/backup_slices/My/SetUp.png" mode="" @click="Setup()"></image>
			</view>
			
			<!-- 头像 -->
			<view class="HeadPortrait flex-column align-items">
				<image class="headPortrait" src="../../static/backup_slices/My/Tx.png" mode="" @click="headPortrait()"></image>
				<text class="font-24 color-f">未来</text>
			</view>
			
			<!-- 钱包 奖励金 优惠券 -->
			<view class="Money flex justify-content">
				<view class="li flex-column align-items">
					<text class="font-30">0</text>
					<text class="font-28">钱包</text>
				</view>
				<view class="li flex-column align-items">
					<text class="font-30">0</text>
					<text class="font-28">奖励金</text>
				</view>
				<view class="li flex-column align-items">
					<text class="font-30">0</text>
					<text class="font-28">优惠券</text>
				</view>
			</view>
		
		</view>
		<!-- 我的订单 -->
		<view class="Order flex-column">
			<view class="order flex space-between align-items background-f">
				<text class="font-24">我的订单</text>
				<text class="font-24">查看更多详情</text>
			</view>
			<view class="payment flex background-f">
				<view class="Li flex-column align-items" v-for="(item,index) in Payment" :key="index" @click="Order(index)">
					<image class="ing" :src="item.img" mode=""></image>
					<text class="font-28">{{item.Name}}</text>
				</view>
			</view>
		</view>
		<!-- 选项 -->
		<view class="Option flex-column">
			<view class="option flex background-f" v-for="(item,index) in Option" :key="index">
				<view class="li flex-column align-items" v-for="(iem,iex) in item" :key="iex" @click="Appraisal(index,iex)">
					<image class="ing" :src="iem.img" mode=""></image>
					<text class="font-28">{{iem.Name}}</text>
				</view>
			</view>
		</view>
		<!-- 电话 -->
		<view class="Telephonec font-24 flex justify-content">
			<text>客服电话：</text>
			<text>400 086 5285</text>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				Payment:[
					{'img':'../../static/backup_slices/My/Payment.png','Name':'待支付'},
					{'img':'../../static/backup_slices/My/DeliverGoods.png','Name':'待发货'},
					{'img':'../../static/backup_slices/My/ReceivingGoods.png','Name':' 待收货'},
					{'img':'../../static/backup_slices/My/AfterSale.png','Name':'售后'}
				],
				Option: [
					[
						{'img':'../../static/backup_slices/My/Appraisal.png','Name':'我的鉴定'},
						{'img':'../../static/backup_slices/My/recovery.png','Name':'我的回收'},
						{'img':'../../static/backup_slices/My/Curing.png','Name':' 我的养护'}
					],
					[
						{'img':'../../static/backup_slices/My/goods.png','Name':'我的找货 '},
						{'img':'../../static/backup_slices/My/Shop.png','Name':'我的店铺'},
						{'img':'../../static/backup_slices/My/Opinion.png','Name':'意见反馈'}
					]
				]
			}
		},
		onLoad () {
		},
		methods: {
			// 设置
			Setup () {
				uni.navigateTo({
					url:'/pages/My/Shezhi/Shezhi'
				})
			},
			// 头像
			headPortrait () {
				uni.navigateTo({
					url:'/pages/My/Data/Data'
				})
			},
			//订单
			Order (e) {
				if(e === 0){
					uni.navigateTo({
						url:'/pages/My/Purchase/Purchase?id=1'
					})
				}else if(e === 1){
					uni.navigateTo({
						url:'/pages/My/Purchase/Purchase?id=2'
					})
				}else if(e === 2){
					uni.navigateTo({
						url:'/pages/My/Purchase/Purchase?id=3'
					})
				}
			},
			//鉴定
			Appraisal(index,iex){
				console.log(index,iex)
				if(index === 0 && iex ===0){
					uni.navigateTo({
						url:'/pages/My/Appraisal/Appraisal'
					})
				}
			}
		}
	}
</script>

<style lang="scss">
	.My{
		background: #F5F5F5;
		// 头像设置
		.Head{
			width: 100%;
			height: 386upx;
			background: url(../../static/backup_slices/My/Background.png) no-repeat center;
			background-size: 100% 386upx;
			// 设置
			.SetUp{
				margin: 22upx 0 13upx 0;
				flex-direction: row-reverse;
				height: 42upx;
				.iag{
					margin: 0 22upx 0 33upx;
					width: 44upx;
					height: 34upx;
				}
				.ibg{
					height: 42upx;
					width: 42upx;
				}
			}
			// 头像
			.HeadPortrait{
				.headPortrait{
					margin-bottom: 10upx;
					width: 100upx;
					height: 100upx;
					background: #FFFFFF;
					border-radius: 50%;
				}
			}
			// 钱包 奖励金 优惠券
			.Money{
				margin-top: 68upx;
				.li{
					width: 200upx;
					color: #FD9226;
					text:nth-child(1){
						margin-bottom: 24upx;
						height: 24upx;
						line-height: 24upx;
					}
					text:nth-child(2){
						height: 28upx;
						line-height: 28upx;
					}
				}
			}
		}
		// 我的订单
		.Order{
			margin: 30upx 0 26upx 0;
			height: 270upx;
			.order{
				padding: 0 43upx 0 45upx;
				height: 80upx;
				color: #101010;
			}
			.payment{
				margin-top: 2upx;
				height: 186upx;
				.Li{
					width: 187upx;
					color: #101010;
					.ing{
						margin: 48upx 0 30upx 0;
						height: 58upx;
						width: 58upx;
					}
					text{
						height: 28upx;
						line-height: 28upx;
					}
				}
			}
		}
		// 选项
		.Option{
			height: 410upx;
			.option{
				height: 200upx;
				margin-bottom: 2upx;
				.li{
					width: 250upx;
					.ing{
						margin:38upx 0;
						height: 56upx;
						width: 56upx;
					}
					text{
						height: 28upx;
						line-height: 28upx;
					}
				}
			}
		}
		// 电话
		.Telephonec{
			flex: 1;
			align-items: flex-end;
			text{
				margin-bottom: 20upx;
				height: 24upx;
				line-height: 24upx;
			}
		}
	}
</style>
