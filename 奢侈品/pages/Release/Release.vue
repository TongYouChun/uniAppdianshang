<template>
	<view class="Release flex-column height">
		<view class="recovery li flex align-items">
			<image class="ing" src="../../static/backup_slices/fabu/huisho.png" mode=""></image>
			<view class="TexT flex-column">
				<text class="font-28">平台回收</text>
				<text class="font-24">图片鉴定初步估计，买进同意再邮寄给...</text>
			</view>
		</view>
		<view class="Consignment li flex align-items">
			<image class="ing" src="../../static/backup_slices/fabu/goumai.png" mode=""></image>
			<view class="TexT flex-column">
				<text class="font-28">平台寄售</text>
				<text class="font-24">平台托管服务，帮您推广营销，省心...</text>
			</view>
		</view>
		<view class="Release li flex align-items">
			<image class="ing" src="../../static/backup_slices/fabu/tubiaozhizuomoban.png" mode=""></image>
			<view class="TexT flex-column">
				<text class="font-28">自由发布</text>
				<text class="font-24">自由发布，自由定价，定价多少得多少</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style lang="scss">
	.Release{
		background: #F5F5F5;
		.li{
			width: 100%;
			height: 184upx;
			background: #FFFFFF;
			margin: 20upx 0 30upx 0;
			.ing{
				margin: 0 32upx 0 65upx;
				width: 95upx;
				height: 95upx;
			}
		}
	}
</style>
