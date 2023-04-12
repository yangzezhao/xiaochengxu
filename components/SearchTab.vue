<template>
	<view class="search-tab">
		<view class="select-nav">
			<view class="sn-item" v-for="item in selectNav" @click="openItem(item.id)" :class="checkItemId == item.id ?'sn-item-active':''">
				<text>
					{{item.name}}
				</text>
				<u-icon name="arrow-down-fill" size="14" class="sn-icon"></u-icon>
			</view>
		</view>
		<view class="select-main" v-if="mainShow">
			<view class="sm-title">
				<view class="sm-title-item" v-for="item in selectNav" @click="getMainList(item.id)" :class="checkTitleId == item.id ?'sm-title-item-active':''">
					<text>{{item.name}}</text>
				</view>
			</view>
			<view class="sm-main">
				<view class="sm-main-item" v-for="item in selectNav" @click="clickValue(item.name)" :class="checkValue == item.name ?'sm-item-active':''">
					<text>{{item.name}}</text>
				</view>
			</view>
		</view>
		<!-- 更多筛选 -->
		<u-mask :show="showValue || mainShow " z-index="98"></u-mask>
		<view class="select-more" v-if="showValue">
			<scroll-view :scroll-top="0" scroll-y="true" class="scroll-Y">
			<view class="smore-main">
				<view class="smore-item" v-for="item in moreList">
					<view class="smore-title">
						<text>{{item.title}}</text>
					</view>
					<view class="smore-value">
						<view class="smore-value-item" 
						v-for="it in item.children" @click="clickMore(item.mid,it.mcid)"
						:class="[moreValue[0]== it.mcid ? 'active' : '',moreValue[1]== it.mcid ? 'active' : '',moreValue[2]== it.mcid ? 'active' : '']">
							{{it.name}}
						</view>
					</view>
				</view>
			</view>
			<view class="smore-bottom">
				<view class="resetting" @click="resetting">
					<text>重置</text>
				</view>
				<view class="confirm">
					<text>确认</text>
				</view>
			</view>
			</scroll-view>
		</view>
	</view>
</template>

<script>
	export default{
		props:{
			selectNav:{
				type:Array,
				default:()=>[]
			},
			moreList:{
				type:Array,
				default:()=>[]
			},
			mnum:{
				type:Number,
				default:0
			}
		},
		data() {
			return {
				show:true,
				//筛选页面高度
				mainShow:false,
				//点击的分类id
				checkItemId:0,
				//点击左侧范围的id
				checkTitleId:0,
				//选择内容
				checkValue:"",
				showValue:false,
				//更多数组
				moreValue:new Array(this.mnum)
			}
		},
		methods: {
			openItem(id){
				if(this.checkItemId == id){
					this.mainShow = false
					this.showValue = false
					this.checkItemId = 0
				}else{
					this.mainShow = false
					this.showValue = false
					if(id != 4){
						this.mainShow = true
						this.checkItemId = id
					}else{
						
						this.checkItemId = id
						this.showValue = true
					}
				}
			},
			getMainList(id){
				this.checkTitleId = id
			},
			clickValue(val){
				this.checkValue = val
			},
			clickMore(mid,id){
				let idx = 0
				this.moreList.forEach((item,index)=>{
					if(mid == item.mid){
						idx = index
					}
				})
				
				this.$set(this.moreValue, idx, id)
				
			},
			//重置更多选择
			resetting(){
				this.moreValue = []
			}
			//确认更多选择，回传到父组件
			
		}
	}
</script>

<style lang="scss" scoped>
.search-tab{
	.select-nav{
		position: relative;
		z-index: 99;
		display: flex;
		padding:0 30rpx;
		// margin-left: 30rpx;
		height: 80rpx;
		line-height: 80rpx;
		background-color: #fff;
		justify-content: space-between;
		font-size: 28rpx;
		.sn-item{
			display: flex;
			align-items: center;
			// justify-content: center;
			&.sn-item-active{
				color: #429EFD;
				.sn-icon{
					transform: rotate(180deg);
				}
			}
		}
		.sn-icon{
			margin-left: 10rpx;
			
		}
	}
	.select-main{
		background-color: #fff;
		position: absolute;
		z-index: 99;
		display: flex;
		.sm-title{
			background: #f8f8f9;
			font-size: 26rpx;
			width: 180rpx;
			.sm-title-item{
				padding-left: 30rpx;
				height: 80rpx;
				line-height: 80rpx;
				&.sm-title-item-active{
					background-color: #fff;
				}
			}
		}
		.sm-main{
			flex: 5;
			display: flex;
			flex-wrap: wrap;
			align-content:flex-start;
			padding-left: 40rpx;
			.sm-main-item{
				margin: 0 15rpx;
				margin-top: 30rpx;
				height: 70rpx;
				width: 146rpx;
				text-align: center;
				line-height: 70rpx;
				background-color: #F7F8FA;
				border-radius: 4rpx;
				&.sm-item-active{
					background-color: #429EFD;
					color: #fff;
				}
			}
		}
	}
	.select-more{
		position: absolute;
		z-index: 99;
		background-color: #fff;
		padding-top: 14rpx;
		.scroll-Y{
			height: 80vh;
		}
		.smore-main{
			padding: 0 30rpx;
			.smore-item{
				.smore-title{
					font-size: 32rpx;
					font-family: PingFang SC, PingFang SC-Semibold;
					font-weight: 600;
					color: #121212;
					margin-bottom: 36rpx;
				}
				.smore-value{
					display: flex;
					flex-wrap: wrap;
					// justify-content: space-between;
					.smore-value-item{
						// flex: 1;
						width: 154rpx;
						height: 70rpx;
						line-height: 70rpx;
						background: #f7f8fa;
						border-radius: 2px;
						text-align: center;
						margin-right: 18rpx;
						margin-bottom: 30rpx;
						&.active{
							background: #429EFD;
							color: #fff;
						}
					}
				}
			}
		}
		.smore-bottom{
			display: flex;
			height: 173rpx;
			line-height: 173rpx;
			padding: 0 30rpx;
			justify-content: space-between;
			.resetting,.confirm{
				width: 318rpx;
				height: 80rpx;
				line-height: 80rpx;
				text-align: center;
				font-size: 28rpx;
				border-radius: 16rpx;
			}
			.resetting{
				border: 2rpx solid #c8c8c8;
			}
			.confirm{
				background-color: #429EFD;
				color: #fff;
			}
		}
	}
}
</style>