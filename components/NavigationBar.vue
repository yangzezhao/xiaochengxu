<template>
	<view class="NavigationBar" :style="[{'padding-top':`${height.customBar}rpx`}]">
		<view class="nb-top"
		:style="[{'height':`${height.customBar}rpx`},{'line-height':`${height.customBar}rpx`}]">
			<!-- <view class="nb-main">
				<text>贵阳</text>
			</view> -->
		</view>
		<view class="nb-search">
			<view class="nb-s-main">
				<u-icon size="30" color='#AAA6B9' name="search"></u-icon>
				<u-input v-model="keyword" :type="keyword" class="nb-s-s"/>
			</view>
		</view>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				height:{
					statusBar:0,
					customBar:0,
					navbar:0,
				},
				keyword:'',
			}
		},
		created() {
			this.getSystemH()
		},
		methods:{
			getSystemH(){
				uni.getSystemInfo({
					success: (e) => {
					  // this.compareVersion(e.SDKVersion, '2.5.0')
					  let statusBar = 0  //状态栏高度
					  let customBar = 0  // 状态栏高度 + 导航栏高度  
					  let navbar = 0 // 自定义标题与胶囊对齐高度
					  // #ifdef MP-WEIXIN
					  statusBar = e.statusBarHeight
					  const custom = wx.getMenuButtonBoundingClientRect()
					  customBar = custom.bottom + custom.top - e.statusBarHeight
					  navbar = (custom.top - e.statusBarHeight) * 2 + custom.height
					  this.height.statusBar = statusBar
					  this.height.customBar = customBar
					  this.height.navbar = navbar
					  console.log(statusBar,customBar,navbar)
					  // #endif
					}
				})
			},
		},
	}
</script>

<style lang="scss" scoped>
	.NavigationBar{
		position: relative;
		z-index: 99;
		padding:0 30rpx;
		background: radial-gradient(#bcdffd, rgb(205,244,246));
		.nb-search{
			padding: 20rpx 0;
			// padding-bottom: 14rpx;
			.nb-s-main{
				display: flex;
				align-items: center;
				padding: 0 30rpx;
				height: 80rpx;
				background: #ffffff;
				border-radius: 20rpx;
				.nb-s-s{
					flex: 1;
					margin-left: 20rpx;
				}
			}
		}
		
	}
</style>