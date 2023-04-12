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
						<text>{{item.name}}</text>
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
					<view class="corporation-name">
						<text>{{item.intention}}</text>
					</view>
					<view class="corporation-address">
						<text>{{item.date}}</text>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	const list = [
		{
			id:'2001',
			name:'张小静',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'贵阳',
				'本科',
				'全职',
			],
			intention:'UI设计师',
			date:'2023-01-28',
		},{
			id:'2001',
			name:'张小静',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'贵阳',
				'本科',
				'全职',
			],
			intention:'UI设计师',
			date:'2023-01-28',
		},{
			id:'2001',
			name:'张小静',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'贵阳',
				'本科',
				'全职',
			],
			intention:'UI设计师',
			date:'2023-01-28',
		},{
			id:'2001',
			name:'张小静',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'贵阳',
				'本科',
				'全职',
			],
			intention:'UI设计师',
			date:'2023-01-28',
		},{
			id:'2001',
			name:'张小静',
			price:'8-10.13薪水',
			label:[
				'1-3年',
				'贵阳',
				'本科',
				'全职',
			],
			intention:'UI设计师',
			date:'2023-01-28',
		},
	]
	const Nav = [
		{
			id:1,
			name:'职能'
		},
		{
			id:2,
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
			mid:11001,
			children:[
				{name:'不限',mcid:0},
				{name:'无工作经验',mcid:10003},
				{name:'1年以内',mcid:10004},
				{name:'2年以内',mcid:10005},
				{name:'3年以内',mcid:10006},
				{name:'4年以内',mcid:10007},
				{name:'5年以内',mcid:10008},
				{name:'6年以内',mcid:10009},
				{name:'7年以内',mcid:10010},
			]
		},
		{
			title:'学历要求',
			mid:12001,
			children:[
				{name:'不限',mcid:0},
				{name:'学历不限',mcid:10013},
				{name:'初中',mcid:10014},
				{name:'高中',mcid:10015},
				{name:'大专',mcid:10016},
				{name:'本科',mcid:10017},
			]
		},
		{
			title:'年龄要求',
			mid:13001,
			children:[
				{name:'不限',mcid:10022},
				{name:'16-20岁',mcid:10023},
				{name:'20-30岁',mcid:10024},
				{name:'30-35岁',mcid:10025},
				{name:'35-40岁',mcid:10026},
				{name:'40-45岁',mcid:10027},
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
				Nav,
				mList,
				list,
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
				margin-bottom: 40rpx;
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
				border-top: 2rpx solid #c8c8c8;
				padding: 31rpx 0;
				// padding-bottom: 33rpx;
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
