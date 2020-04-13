<template>
	<view class="classification flex-column height">
		<!-- 搜索 -->
		<view class="search flex space-between align-items background-f">
			<view class="search_Left flex align-items">
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/search-icon.png" mode=""></image>
				<input class="input font-28" type="text" value="" placeholder="搜你想要的东东"/>
			</view>
			<view class="search_right">
				<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/message-icon.png" mode=""></image>
			</view>
		</view>
		<!-- 内容 -->
		<view class="content flex">
			<view class="option flex-column">
				<view class="li font-28 color-3 flex justify-content align-items" :class="{Te:index === tabCurrentIndex}" v-for="(item,index) in Li" :key="index" @click="Option(index)">
					{{item}}
				</view>
			</view>
			<view class="information flex-column flex-overflow">
				<!-- 品牌 -->
				<Brand v-if="judge === 0"></Brand>
				<!-- 热门大牌 -->
				<Popular v-if="judge === 1"></Popular>
				<!-- 名包 -->
				<Package v-if="judge === 2"></Package>
				<!-- 腕表 -->
				<Surface v-if="judge === 3"></Surface>
				<!-- 珠宝首饰 -->
				<Jewellery v-if="judge === 4"></Jewellery>
				<!-- 名鞋 -->
				<Shoes v-if="judge === 5"></Shoes>
				<!-- 二手中古 -->
				<Used v-if="judge === 6"></Used>
			</view>
		</view>
	</view>
</template>

<script>
	import Brand from '../../components/classification/Brand.vue';
	import Popular from '../../components/classification/Popular.vue';
	import Package from '../../components/classification/Package.vue';
	import Surface from '../../components/classification/Surface.vue'
	import Jewellery from '../../components/classification/Jewellery.vue';
	import Shoes from '../../components/classification/Shoes.vue';
	import Used from '../../components/classification/Used.vue'
	export default {
		data() {
			return {
				judge: 0,
				tabCurrentIndex: 0,
				Li:['品牌','热门大牌','名包','腕表','珠宝首饰','名鞋','二手中古']
			}
		},
		components:{
			Brand,
			Popular,
			Package,
			Surface,
			Jewellery,
			Shoes,
			Used
			
		},
		methods: {
			Option (e) {
				this.judge = e;
				this.tabCurrentIndex = e;
			}
		}
	}
</script>

<style lang="scss">
	.classification{
		// 搜索
		.search{
			width: 100%;
			height: 116upx;
			.search_Left{
				margin-left: 36upx;
				width: 620upx;
				height: 76upx;
				box-shadow:0px 2px 8px 0px rgba(204,204,204,0.5);
				border-radius: 20upx;
				.img{
					margin: 0 13upx 0 22upx;
					width: 32upx;
					height: 30upx;
				}
				.input{
					height: 52upx;
					width: 100%;
				}
			}
			.search_right{
				.img{
					margin-right: 28upx;
					width: 35upx;
					height: 38upx;
				}
			}
		}
		// 内容
		.content{
			flex: 1;
			.option{
				width: 150upx;
				height: 100%;
				background: #F5F5F5;
				.li{
					height: 112upx;
				}
				.Te{
					color: #FFA732;
					border-left: 6upx solid #FFA732;
					background: #FFFFFF;
				}
			}
			.information{
			}
		}
	}
</style>
