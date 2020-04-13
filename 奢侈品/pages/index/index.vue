<template>
	<view class="index_content flex-column height">
		<view class="index flex-column">
			<!-- 搜索 -->
			<view class="search flex space-between align-items background-f">
				<view class="search_Left flex align-items">
					<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/search-icon.png" mode=""></image>
					<input class="input font-24" type="text" value="" placeholder="热门“AJ疯抢999元”"/>
				</view>
				<view class="search_right">
					<image class="img" src="../../static/backup_slices/mipmap-xxhdpi/message-icon.png" mode=""></image>
				</view>
			</view>
			<view class="content flex-column  flex-overflow">
				<Homepage></Homepage>
			</view>
		</view>
		
	</view>
</template>

<script>
	import Homepage from "../../components/index/Homepage.vue";
	export default {
		data() {
			return {
			}
		},
		components:{
			Homepage
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.index_content{
		margin-top: 20upx;
		.index{
			flex: 1;
			background: #F5F5F5;
			 // 搜索
			.search{
				width: 100%;
				height: 88upx;
				.search_Left{
					margin-left: 36upx;
					width: 620upx;
					height: 52upx;
					background: #F5F5F5;
					border: 1upx solid #101010;
					border-radius: 8upx;
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
		}
		.content{
			flex: 1;
		}
	}
</style>
