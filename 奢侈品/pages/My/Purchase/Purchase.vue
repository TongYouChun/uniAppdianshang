<template>
	<view class="Purchase flex-column height">
		<!-- 选项 -->
		<view class="Option flex">
			<!-- 全部  待付款 待发货 待收货-->
			<view class="li flex-column align-items justify-content" :class="{Te:index === tabCurrentIndex}" v-for="(item,index) in Caidan" :key="index" @click="Xuanxiang(index)">
				<text class="font-28 color-10">{{item}}</text>
				<text></text>
			</view>
		</view>
		<!-- 全部产品 -->
		<view class="Product flex-column flex-overflow align-items">
			<!-- 全部 -->
			<purchase :Commoditya='Commodity' v-if="Te?false:true"></purchase>
			<!-- 待付款 -->
			<payment :Commodity='Comm' v-if="Te?true: false"></payment>
		</view>
	</view>
</template>

<script>
	import purchase from '../../../components/My/purchase/whole.vue';
	import payment from '../../../components/My/purchase/Payment.vue';
	export default {
		data() {
			return {
				// 菜单
				Caidan: ['全部','待付款','待发货','待收货'],
				tabCurrentIndex: 0,
				//  全部产品
				Te: false,
				Comm: '',
				Commodity: [
					{
						'ing':'../../../static/backup_slices/My/shop-selected.png',
						'Name1':'马切达工作室',
						'ig':'../../../static/backup_slices/mipmap-xxhdpi/you1.png',
						'Name2':'等待买家付款',
						'mg':'../../../static/backup_slices/My/hei.png',
						'TexT':'【19春夏新品】RogerVivier/罗杰· 维维亚女士包袋 Viv 手袋 手提包',
						'TecT':'均码',
						'text':'共一件商品',
						'tect': '3600元',
						'payment1':'取消订单',
						'payment2': '朋友代付',
						'payment3': '付款'
					},
					{
						'ing':'../../../static/backup_slices/My/shop-selected.png',
						'Name1':'马切达工作室',
						'ig':'../../../static/backup_slices/mipmap-xxhdpi/you1.png',
						'Name2':'卖家已发货',
						'mg':'../../../static/backup_slices/My/LV.png',
						'TexT':'Givenchy/纪梵希 女士黑色连帽卫 衣 BW7051 3Z0L 001',
						'TecT':'M码',
						'text':'共一件商品',
						'tect': '900元',
						'payment1':'查看物流',
						'payment2': '延长收货',
						'payment3': '确认收货'
					},{
						'ing':'../../../static/backup_slices/My/shop-selected.png',
						'Name1':'马切达工作室',
						'ig':'../../../static/backup_slices/mipmap-xxhdpi/you1.png',
						'Name2':'买家已付款',
						'mg':'../../../static/backup_slices/My/jimmy choo.png',
						'TexT':'Valentino/华伦天奴 明星同款女士 经典铆钉元素高跟鞋凉鞋细跟鞋女 鞋 RW2S0375-VNW-N91',
						'TecT':'意码35',
						'text':'共一件商品',
						'tect': '1200元',
						'payment1':'查看物流',
						'payment2': '延长收货',
						'payment3': '确认收货'
					}
				],
				// 待付款
				Commodityf:[
					{
						'ing':'../../../static/backup_slices/My/shop-selected.png',
						'Name1':'马切达工作室',
						'ig':'../../../static/backup_slices/mipmap-xxhdpi/you1.png',
						'Name2':'等待买家付款',
						'mg':'../../../static/backup_slices/My/hei.png',
						'TexT':'【19春夏新品】RogerVivier/罗杰· 维维亚女士包袋 Viv 手袋 手提包',
						'TecT':'均码',
						'text':'共一件商品',
						'tect': '3600元',
						'payment1':'取消订单',
						'payment2': '朋友代付',
						'payment3': '付款',
						'like': [{
								'Ig':'../../../static/backup_slices/My/dan.png',
								'tex' : 'SAINT LAURENT PARIS 黑色 女士连衣裙',
								'TexT1':'$1000元',
								'TexT2':'加入购物车',
							},{
								'Ig':'../../../static/backup_slices/My/coco.png',
								'tex' : 'SAINT LAURENT PARIS 黑色 女士连衣裙',
								'TexT1':'$1000元',
								'TexT2':'加入购物车',
							}]
					}
				],
				// 待发货
				Commodityh:[
					{
						'ing':'../../../static/backup_slices/My/shop-selected.png',
						'Name1':'马切达工作室',
						'ig':'../../../static/backup_slices/mipmap-xxhdpi/you1.png',
						'Name2':'卖家已发货',
						'mg':'../../../static/backup_slices/My/LV.png',
						'TexT':'Givenchy/纪梵希 女士黑色连帽卫 衣 BW7051 3Z0L 001',
						'TecT':'M码',
						'text':'共一件商品',
						'tect': '900元',
						'payment1':'查看物流',
						'payment2': '延长收货',
						'payment3': '确认收货',
						'like': [{
								'Ig':'../../../static/backup_slices/My/SAINT LAURENT PARIS.png',
								'tex' : 'SAINT LAURENT PARIS 黑色 女士连衣裙',
								'TexT1':'$1000元',
								'TexT2':'加入购物车',
							},{
								'Ig':'../../../static/backup_slices/My/dan.png',
								'tex' : 'SAINT LAURENT PARIS 黑色 女士连衣裙',
								'TexT1':'$1000元',
								'TexT2':'加入购物车',
							}]
					}
				],
				// 待收货
				Commoditys: [
					{
						'ing':'../../../static/backup_slices/My/shop-selected.png',
						'Name1':'马切达工作室',
						'ig':'../../../static/backup_slices/mipmap-xxhdpi/you1.png',
						'Name2':'买家已付款',
						'mg':'../../../static/backup_slices/My/jimmy choo.png',
						'TexT':'Valentino/华伦天奴 明星同款女士 经典铆钉元素高跟鞋凉鞋细跟鞋女 鞋 RW2S0375-VNW-N91',
						'TecT':'意码35',
						'text':'共一件商品',
						'tect': '1200元',
						'payment1':'查看物流',
						'payment2': '延长收货',
						'payment3': '确认收货',
						'like': [{
								'Ig':'../../../static/backup_slices/My/coco.png',
								'tex' : 'SAINT LAURENT PARIS 黑色 女士连衣裙',
								'TexT1':'$1000元',
								'TexT2':'加入购物车',
							},{
								'Ig':'../../../static/backup_slices/My/SAINT LAURENT PARIS.png',
								'tex' : 'SAINT LAURENT PARIS 黑色 女士连衣裙',
								'TexT1':'$1000元',
								'TexT2':'加入购物车',
							}]
					}
				]
			};
		},
		components:{
			purchase,
			payment
		},
		onLoad (e) {
			console.log( parseInt(e.id))
			this.tabCurrentIndex = parseInt(e.id);
			if( this.tabCurrentIndex === 0 ){
				this.Te = false
			}else if( this.tabCurrentIndex === 1 ){
				this.Te = true;
				this.Comm = this.Commodityf;
			}else if( this.tabCurrentIndex === 2 ){
				this.Te = true;
				this.Comm = this.Commodityh;
			}else if( this.tabCurrentIndex === 3 ){
				this.Te = true;
				this.Comm =  this.Commoditys;
			}
		},
		methods: {
			Xuanxiang (e) {
				this.tabCurrentIndex = e;
				if( this.tabCurrentIndex === 0 ){
					this.Te = false
				}else if( this.tabCurrentIndex === 1 ){
					this.Te = true;
					this.Comm = this.Commodityf;
				}else if( this.tabCurrentIndex === 2 ){
					this.Te = true;
					this.Comm = this.Commodityh;
				}else if( this.tabCurrentIndex === 3 ){
					this.Te = true;
					this.Comm =  this.Commoditys;
				}
			}
		}
	}
</script>

<style lang="scss">
	.Purchase{
		background: #f5f5f5;
		.Option{
			height: 110upx;
			background: #f5f5f5;
			.li{
				width: 187upx;
				height: 110upx;
				text:nth-child(1){
					height: 28upx;
					line-height: 28upx;
				}
			}
			.Te{
				text:nth-child(1){
					color: #FFA732;
				}
				text:nth-child(2){
					margin-top: 10upx;
					width: 60upx;
					height: 2upx;
					background: #FFA732;
				}
			}
		}
		.Product{
			flex: 1;
			
		}
	
	}
</style>
