<template>
	<view class="content">
		<view class="card1" style="padding-top: 50rpx;">
			<view class="head" >
				<view class="name">
					高级产品经理
				</view>
				<view class="time">
					2023年1月12日
				</view>
			</view>
			<view class="bread">
				<view class="breadItem">
					1-3年
				</view>
				<view class="breadItem">
					年终奖金
				</view>
				<view class="breadItem">
					年终奖金
				</view>

			</view>

			<view class="salary">
				8-10k·13薪
			</view>
			<view class="end">
				<view class="address">
					观山湖区 长岭南路
				</view>

				<view class="history">
					浏览量：1232
				</view>
			</view>

		</view>

		<view class="card2">
			<view class="name">
				职位描述
			</view>
			<view class="desc">
				<text>1、负责沟通、收集、确认用户需求。收集产品使用中遇到的问题 挖掘真实业务需求、核心问题所在。</text>
				<text> 2、梳理消费行业，研究竞品，洞察价值需求，制定产品解决方案</text>
				<text>3、与用户、开发人员共同评审用户需求、产品需求，跟进产品需 求开发进度。</text>
				<text> 4、产品上线后，进行产品运营跟踪，分析运营数据，确认预期是 否达成。</text>
				 <text>6、撰写需求收集、业务梳理、功能设计等必要文档。</text>
				 <text>7、通过市场调研、竞品分析，对标我司产品，制定应对策略及改 进方案，确保产品产品核心竞争力、规模化可复制、市场收入可预 期。</text>
				<text> 8、编写产品推广方案，执行产品推广策略。</text>
			</view>
			
			<view class="title">
				岗位要求
			</view>
			<view class="desc">
				<text>1、负责沟通、收集、确认用户需求。收集产品使用中遇到的问题 挖掘真实业务需求、核心问题所在。</text>
				<text> 2、梳理消费行业，研究竞品，洞察价值需求，制定产品解决方案</text>
				<text>3、与用户、开发人员共同评审用户需求、产品需求，跟进产品需 求开发进度。</text>
				<text> 4、产品上线后，进行产品运营跟踪，分析运营数据，确认预期是 否达成。</text>
				 <text>6、撰写需求收集、业务梳理、功能设计等必要文档。</text>
				 <text>7、通过市场调研、竞品分析，对标我司产品，制定应对策略及改 进方案，确保产品产品核心竞争力、规模化可复制、市场收入可预 期。</text>
				<text> 8、编写产品推广方案，执行产品推广策略。</text>
			</view>
			
			
		</view>
	
		<view class="card3">
			<view class="name">
				安全提示
			</view>
			<view class="end">
				<image src="../../static/Frame@2x.png" ></image>
				<view class="detail">
					警示：以招聘为名收取培训费用，提供培训贷款，或在录中过程中需 支付体验、
					服装、押金等费用都属于违法行为，请<text>立即举报</text>
				</view>
			</view>
		</view>
	
		<view class="card4">
			<view class="head">
				<view class="card_name ">
					公司信息
				</view>
				<image src="../../static/return.png" mode=""></image>
			</view>
			
			
			<view class="info">
				<image src="../../static/com_logo.png" mode="" class="company"></image>
				
				<view class="com_detail">
					<view class="com_name">
						云码通数据运营股份有限公司
					</view>
					<view class="com_text">
						贵阳·民营·大数据·50-99人
					</view>
				</view>
			</view>
			<view class="address">
				<view class="card_name ">
					公司地址
				</view>
				<view class="go_here">
					<text>去这里</text><image src="../../static/map_here.png" mode=""></image>
				</view>
			</view>
			
			<view class="here_map">
				<map style="width: 690rpx; height: 400rpx;margin: 18rpx 0;" :latitude="latitude" :longitude="longitude" :markers="covers">
								</map>
			</view>
			
			<view class="person">
				
					<image src="../../static/person.png" mode="" class="com_person"></image>
				
				
				<view class="person_detail">
					<view class="person_name">
						全女士
					</view>
					
					<view class="person_tel">
						139****8845
					</view>
				</view>
				
				
			   <image src="../../static/person_call.png" mode="" class="person_call"></image>
				
				
				
			</view>
		
		
		<view class="photo">
			<view class="head" style="margin-top: 67rpx	;">
				<view class="card_name ">
					企业相册
				</view>
				<image src="../../static/return.png" mode=""></image>
			</view>
			
			<view class="photo_list">
				<image src="../../static/photo.png" mode=""></image>
				<image src="../../static/photo.png" mode=""></image>
				<image src="../../static/photo.png" mode=""></image>
				<image src="../../static/photo.png" mode=""></image>
			</view>
			
		</view>
		
		<view class="commitList">
			<view class="head" style="margin-top: 67rpx	;">
				<view class="card_name ">
					岗位评价
				</view>
				
				<image src="../../static/return.png" mode=""></image>
				
				
			</view>
			<view class="person">
				
					<image src="../../static/person.png" mode="" class="com_person"></image>
				
				
				<view class="person_detail">
					<view class="person_name">
						晓晓
					</view>
					
					<view class="person_tel">
						面试职位：UI/UX设计 <u-rate count="count" current="2" inactive-color="#bbbbbb" ></u-rate>
					</view>
				</view>
				
				
				
				
			   
				
				
				
			</view>
			<view class="" style="background-color: rgb(244, 244, 244);width: 100rpx;margin:20rpx 0; height: 30rpx;font-size: 20rpx;
			margin-left: 119rpx;display: flex;justify-content: center;align-items: center;border-radius: 10rpx;color: #717171;">
				通讯补贴
			</view>
			
			<view class="comm" style="font-weight: bold;font-size: 36rpx;margin-left: 119rpx;">
				氛围好
			</view>
		</view>
		</view>
	
		<view class="footer">
			<view class="collect">
				<image src="../../static/stars.png" mode=""></image>
				收藏
			</view>
			<view class="share">
				<image src="../../static/shares.png" mode=""></image>
				分享
			</view>
			<div style="display: flex;">
				<u-button type="primary" style="margin-left: 88rpx;">立即沟通</u-button>
				<u-button type="primary" disabled style="margin-left: 26rpx;">投递简历</u-button>
			</div>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				count: 4,
				id:0, // 使用 marker点击事件 需要填写id
							title: 'map',
							latitude: 39.909,
							longitude: 116.39742,
							covers: [{
								latitude: 39.909,
								longitude: 116.39742,
								iconPath: '@/static/location.png'
							}, {
								latitude: 39.90,
								longitude: 116.39,
								iconPath: '../../../static/location.png'
							}]
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.content {
		
		background-color: rgb(249, 249, 249);

		.card1 {
			display: flex;
			flex-direction: column;
			justify-content: space-between;
			width: 750rpx;
			margin: 20rpx 0;
			background-color: white;
			padding: 30rpx;

			.head {
				display: flex;
				justify-content: space-between;

				.name {
					font-weight: bold;
					color: #121212;
					font-size: 32rpx;
				}

				.time {
					font-size: 24rpx;
					color: #717171;
				}

			}

			.bread {
				display: flex;
				color: #717171;
				align-items: center;
				margin: 20rpx 0;

				.breadItem {
					font-size: 24rpx;
					height: 40rpx;
					line-height: 40rpx;
					margin-right: 14rpx;
					padding: 0 8rpx;
					background-color: #f4f4f4;
				}
			}

			.salary {
				color: #3FABFF;
				font-size: 32rpx;
			}

			.end {
				display: flex;
				justify-content: space-between;
				font-size: 24rpx;
				color: #717171;
				margin-top: 21rpx;
			}
		}
	
		.card2 {
			
			background-color: white;
			display: flex;
			flex-direction: column;
			padding: 30rpx;
			.name {
				margin: 30rpx 0 ;
				font-weight: bold;
				color: #121212;
				font-size: 32rpx;
			}
			.desc {
				font-size: 24rpx;
				color: #121212;
				display: flex;
				flex-direction: column;
				
				text {
					line-height: 50rpx;
				}
			}
			.title {
				margin: 15rpx;
				font-weight: bold;
			}
		}
	
		.card3 {
			height: 207rpx;
			width: 750rpx;
			background-color: white;
			margin: 20rpx 0;
			padding: 30rpx;
			display: flex;
			flex-direction: column;
			.name {
				// margin: 30rpx 0 ;
				font-weight: bold;
				color: #121212;
				font-size: 32rpx;
			}
			.end {
				margin: 30rpx 0;
				image {
					width: 64rpx;
					height: 64rpx;
				}
				.detail {
					font-size: 24rpx;
					width: 600rpx;
					margin: 0 30rpx;
				}
				display: flex;
			}
		}
	
	
		.card4{
			display: flex;
			background-color: white;
			flex-direction: column;
			padding: 30rpx;
			.head {
				display: flex;
				justify-content: space-between;
				.card_name {
					// margin: 30rpx 0 ;
					font-weight: bold;
					color: #121212;
					font-size: 32rpx;
				}
				image {
					width: 36rpx;
					height: 36rpx;
				}
			}
			
			
			.info {
				margin-top: 30rpx;
				display: flex;
				align-items: center;
				image {
					width: 114rpx;
					height: 114rpx;
				}
				.com_detail {
					padding: 23rpx;
				}
				.com_name {
					font-weight: bold;
					font-size: 32rpx;
					
				}
				
				.com_text {
					margin-top: 21rpx;
					font-size: 24rpx;
				}
			}
		
		
			.address {
				margin-top: 72rpx;
				display: flex;
				justify-content: space-between;
				.card_name {
					font-weight: bold;
					font-size: 32rpx;
					
				}
				.go_here {
					color: #3FADFF;
					image {
						width: 32rpx;
						height: 32rpx;
					}
				}
			}
		
		
			.here_map {
				width: 680rpx;
				height: 400rpx;
				margin: 0 auto;
			}
			.person {
				position: relative;
				margin-top: 56rpx;
				display: flex;
				.com_person {
					width: 90rpx;
					height: 90rpx;
				}
				.person_detail {
					display: flex;
					flex-direction: column;
					justify-content: space-between;
					justify-content: center;
					margin-left: 24rpx;
					
					.person_name {
						font-size: 32rpx;
						font-weight: bold;
					}
					.person_tel {
						margin-top: 10rpx;
						font-size: 28rpx;
						color: #4F4F4F;
					}
				}
				.person_call {
					position: absolute;
					right: 30rpx;
					width: 32rpx;
					height: 32rpx;
				}
				
			}
		
			.photo {
				display: flex;
				flex-direction: column;
				.photo_list {
					margin-top: 40rpx;
					width: 750rpx;
					white-space: nowrap;
					overflow-x: auto;
					  display: -webkit-box;
					  -webkit-overflow-scrolling: touch;
					
					image {
						display: inline-block;
						margin-right: 40rpx;
						width: 276rpx;
						height: 262rpx;
						border-radius: 10rpx;
					}
				}
			}
			
			.commitList {
				margin-bottom: 120rpx;
			}
			
		}
		.footer {
			position: fixed;
			bottom: 50px ;
			display: flex;
			align-items: center;
			width: 750rpx;
			height: 150rpx;
			background-color: white;
			.collect {
				display: flex;
				margin-left: 36rpx;
				flex-direction: column;
				image {
					width: 44rpx;
					height: 44rpx;
				}
			}
			.share {
				margin-left: 56rpx;
				display: flex;
				flex-direction: column;
				display: flex;
				image {
					width: 44rpx;
					height: 44rpx;
				}
			}
			.u-button {
				width: 213rpx;
				height: 80rpx;
				
			}
			
			font-size: 28rpx;
		}
	}
</style>
