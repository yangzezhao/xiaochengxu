<template>
	<view class="content">
		<view class="search-header">
			<NavigationBar></NavigationBar>
			<SearchTab :selectNav="Nav" :moreList="mList" :mnum="mList.length"></SearchTab>
		</view>
		<view class="search-list">
			<view class="search-item" v-for="item in list">
				<view class="sit-header df">
					<view class="sit-title">
						<text>{{item.title}}</text>
					</view>
					<view class="sit-price" style="color: #3FABFF;">
						<text>{{item.price}}</text>
					</view>
				</view>
				<view class="df sit-label">
					<view class="label-item" v-for="label in item.label">
						<text>{{label}}</text>
					</view>
				</view>
				<view class="df sit-corporation">
					<view class="corporation-icon">
						<u-image width="88rpx" height="88rpx" :src="src"></u-image>
					</view>
					<view class="corporation-name">
						<text>{{item.corporation}}</text>
					</view>
					<view class="corporation-address">
						<text>{{item.address}}</text>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	const list = [
		{
			id:'1001',
			title:'UI/UE设计师',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'本科',
				'三维设计',
				'界面设计',
				'APP端',
			],
			corporation:'云码通',
			address:'观山湖区 长岭南路',
		},
		{
			id:'1002',
			title:'UI/UE设计师',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'本科',
				'三维设计',
				'界面设计',
				'APP端',
			],
			corporation:'云码通',
			address:'观山湖区 长岭南路',
		},
		{
			id:'1003',
			title:'UI/UE设计师',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'本科',
				'三维设计',
				'界面设计',
				'APP端',
			],
			corporation:'云码通',
			address:'观山湖区 长岭南路',
		},{
			id:'1004',
			title:'UI/UE设计师',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'本科',
				'三维设计',
				'界面设计',
				'APP端',
			],
			corporation:'云码通',
			address:'观山湖区 长岭南路',
		}
	]
	const Nav = [
		{
			id:1,
			name:'区域'
		},
		{
			id:2,
			name:'行业'
		},
		{
			id:3,
			name:'薪资'
		},
		{
			id:4,
			name:'其他'
		}
	]
	const mList = [
		{
			title:'工作经验',
			mid:14001,
			children:[
				{name:'不限',mcid:10032},
				{name:'无工作经验',mcid:10033},
				{name:'1年以内',mcid:10034},
				{name:'2年以内',mcid:10035},
				{name:'3年以内',mcid:10036},
				{name:'4年以内',mcid:10037},
				{name:'5年以内',mcid:10038},
				{name:'6年以内',mcid:10039},
			]
		},
		{
			title:'职位性质',
			mid:15001,
			children:[
				{name:'不限',mcid:10042},
				{name:'全职',mcid:10043},
				{name:'兼职',mcid:10044},
			]
		},
	]
	import NavigationBar from '@/components/NavigationBar.vue'
	import SearchTab from '@/components/SearchTab.vue'
	export default {
		components:{
			NavigationBar,
			SearchTab
		},
		data() {
			return {
				list,
				Nav,
				mList,
				src: 'https://cdn.uviewui.com/uview/example/fade.jpg'
			}
		},
		onLoad() {

		},
		methods: {
			
		}
	}
</script>
<style>
	page{
		background-color: #F6F9FF;
	}
</style>
<style lang="scss" scoped>
.df{
	display: flex;
}
.content{
	margin-top: 340rpx;
	.search-header{
		position: fixed;
		top:0;
		width: 100%;
		z-index: 99;
	}
	.search-list{
		.search-item{
			background-color: #fff;
			margin: 20rpx 30rpx;
			padding: 0 30rpx;
			.sit-header{
				justify-content: space-between;
				padding: 27rpx 0;
				font-size: 32rpx;
				font-weight: 600;
			}
			.sit-label{
				margin-bottom: 28rpx;
				.label-item{
					margin-right: 14rpx;
					height: 40rpx;
					line-height: 40rpx;
					line-height: 40rpx;
					background: #f4f4f4;
					border-radius: 4rpx;
					padding:0 10rpx;
				}
			}
			.sit-corporation{
				align-items: center;
				padding-bottom: 33rpx;
				.corporation-name{
					color: #121212;
					font-size: 28rpx;
					font-weight: 600;
					margin: 0 14rpx;
				}
				.corporation-address{
					flex: 1;
					text-align: right;
					color: #717171;
					font-size: 24rpx;
				}
			}
		}
	}
}
</style>
