<template>
	<view class="Curing flex-column height">
		<!-- 背景图 -->
		<view class="chart flex-column">
			<image class="Img" src="../../static/backup_slices/mipmap-xxhdpi/yanghu/banner.png" mode=""></image>
		</view>
		
		<!-- 选择 -->
		<view class="Choice flex background-f">
			<view class="li flex justify-content align-items" :class="{Te:index === Indexes}" v-for="(item,index) in uTexT" :key="index" @click="Choice(index)">
				<text class="font-24 color-10">{{item}}</text>
			</view>
		</view>
		<!-- 内容 -->
		<view class="Content flex-column flex-overflow">
			<Curing :ContentTexT = 'ContentTexT'></Curing>
		</view>
	</view>
</template>

<script>
	import Curing from '../../components/index/Curing.vue'
	export default {
		data() {
			return {
				// 选择
				uTexT:['包包养护','鞋靴养护','腕表养护','首饰养护','配饰养护'],
				Indexes: 0,
				
				// 内容
				ContentTexT:[
					{
						ing: '../../static/backup_slices/mipmap-xxhdpi/yanghu/ciqing.png',
						TexT1:'奢品/至一 精致刺绣养护维修',
						TexT2:'破损处定制刺绣/消毒杀菌',
						qian: '400',
						text:'咨询订购',
						Li:[{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/quanwei.png',
							text:'权威质检'
						},{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/fengxiang.png',
							text:'分享'
						},{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/shocang.png',
							text:'收藏商品'
						}]
					},{
						ing: '../../static/backup_slices/mipmap-xxhdpi/yanghu/laling.png',
						TexT1:'奢品/至一 更换维修拉链',
						TexT2:'破损处定制刺绣/消毒杀菌',
						qian: '600',
						text:'咨询订购',
						Li:[{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/quanwei.png',
							text:'权威质检'
						},{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/fengxiang.png',
							text:'分享'
						},{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/shocang.png',
							text:'收藏商品'
						}]
					},{
						ing: '../../static/backup_slices/mipmap-xxhdpi/yanghu/qianbao.png',
						TexT1:'奢品/至一 钱包小皮具精致养护',
						TexT2:'破损处定制刺绣/消毒杀菌',
						qian: '500',
						text:'咨询订购',
						Li:[{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/quanwei.png',
							text:'权威质检'
						},{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/fengxiang.png',
							text:'分享'
						},{
							ig:'../../static/backup_slices/mipmap-xxhdpi/yanghu/shocang.png',
							text:'收藏商品'
						}]
					}
				]
			}
		},
		components:{
			Curing
		},
		onLoad() {
			
		},
		methods: {
			Choice(e){
				this.Indexes = e
			}
		}
	}
</script>

<style lang="scss">
	.Curing{
		background: #f5f5f5;
		// 背景图
		.chart{
			width: 100%;
			height: 240upx;
			.Img{
				width: 100%;
				height: 240upx;
			}
		}
		// 选择
		.Choice{
			height: 71upx;
			.li{
				flex: 1;
				text{
					height: 69upx;
					line-height: 69upx;
				}
			}
			.Te{
				text{
					color: #FF9E24;
					border-bottom: 2upx solid #FF9E24;
				}
			}
		}
	}
</style>
