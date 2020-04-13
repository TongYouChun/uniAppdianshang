<template>
	<view class="Appraisal height flex-column align-items">
		<!-- 选项 -->
		<view class="Option flex justify-content">
			<view class="option flex space-between">
				<view class="li" :class="{Te:inex === uTexT}" v-for="(item,inex) in option" :key="inex" @click="Appraisal(inex)">
					<view class="text flex-column align-items space-between font-28">
						<text>{{item}}</text>
						<text></text>
					</view>
				</view>
			</view>
		</view>
		<!-- 全部商品 -->
		<view class="Commodity flex-column flex-overflow">
			<!-- 图片鉴定 -->
			<Picture v-if="Dtu?0:1"></Picture>
			<!-- 实物鉴定 -->
			<Thing v-if="Dtu?1:0"></Thing>
		</view>
	</view>
</template>

<script>
	import Picture from '../../../components/My/Appraisal/Picture';
	import Thing from '../../../components/My/Appraisal/Thing';
	export default {
		data() {
			return {
				// 选项
				option: ['图片鉴定','实物鉴定'],
				uTexT: 0,
				// 鉴定
				Dtu: 0
			}
		},
		components: {
			Picture,
			Thing
		},
		methods: {
			Appraisal (e) {
				this.uTexT = e;
				this.Dtu = e;
			}
		}
	}
</script>

<style lang="scss">
	.Appraisal{
		background: #f5f5f5;
		// 选项
		.Option{
			width: 100%;
			.option{
				margin: 60upx 0 48upx 0;
				width: 448upx;
				.li{
					width: 154upx;
					.text{
						width: 224upx;
						height: 50upx;
						color: #333;
					}
				}
				.Te{
					text:nth-child(1){
						color: #FFA732;
					}
					text:nth-child(2){
						height: 2upx;
						width: 114upx;
						background: #FFA732;
					}
				}
			}
		}
		.Commodity{
			
		}
	}
</style>
