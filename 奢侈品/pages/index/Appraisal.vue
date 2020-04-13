<template>
	<view class="Appraisal flex-column height">
		<!-- 鉴定内容 -->
		<view class="Content flex-column flex-overflow">
			<!-- 鉴定信息 -->
			<Service :ContentTexT ="ContentTexT"></Service>
		</view>
	</view>
</template>

<script>
	import Service from '../../components/index/service.vue';
	export default {
		data() {
			return {
				ContentTexT: [
					{
						ing:'../../static/backup_slices/mipmap-xxhdpi/tuoyuan.png',
						Name:'大牛',
						shijian:'2019-6-25',
						cakan:'../../static/backup_slices/mipmap-xxhdpi/yanjing.png',
						cakantext:'2798',
						xingxi:'../../static/backup_slices/mipmap-xxhdpi/xingxi.png',
						xingxitext:'2798',
						TexT:'请大神帮忙鉴定Tiffany的手链！！！！',
						Ig:['../../static/backup_slices/mipmap-xxhdpi/1.png','../../static/backup_slices/mipmap-xxhdpi/2.png','../../static/backup_slices/mipmap-xxhdpi/3.png','../../static/backup_slices/mipmap-xxhdpi/4.png','../../static/backup_slices/mipmap-xxhdpi/5.png','../../static/backup_slices/mipmap-xxhdpi/6.png'],
						ig:'../../static/backup_slices/mipmap-xxhdpi/duixiang.png',
						text:'古驰'
					},{
						ing:'../../static/backup_slices/mipmap-xxhdpi/tuoyuan (2).png',
						Name:'罗马明',
						shijian:'2019-6-25',
						cakan:'../../static/backup_slices/mipmap-xxhdpi/yanjing.png',
						cakantext:'2798',
						xingxi:'../../static/backup_slices/mipmap-xxhdpi/xingxi.png',
						xingxitext:'2798',
						TexT:'小ck从朋友那里便宜入手，想知道真假， 特来请老师帮忙鉴定一下。',
						Ig:['../../static/backup_slices/mipmap-xxhdpi/2.1.png','../../static/backup_slices/mipmap-xxhdpi/2.2.png','../../static/backup_slices/mipmap-xxhdpi/2.3.png','../../static/backup_slices/mipmap-xxhdpi/2.4.png','../../static/backup_slices/mipmap-xxhdpi/2.5.png','../../static/backup_slices/mipmap-xxhdpi/2.6.png'],
						ig:'../../static/backup_slices/mipmap-xxhdpi/duixiang.png',
						text:'CK'
					}
				]
			}
		},
		components:{
			Service
		},
		onLoad() {
	
		},
		methods: {
	
		}
	}
</script>

<style lang="scss">
	.Appraisal{
		background: #f5f5f5;
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
		.Content{
		}
	}
</style>
