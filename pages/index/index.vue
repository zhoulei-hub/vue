<template>
	<view style="background-color: #FFD100; height: 999px;">
			<van-row v-if="scrollTop<65" class="cc">
			  <van-col  span="24" >
				  <view  @click="linkTo('../address/address')">
					  <van-icon name="location-o"  size="20px"/>
				  {{address}}
				  </view>
			  </van-col>
			</van-row>
			<van-row v-else class="cc1">
			  <van-col  span="24" >
				 <van-search custom-class="search2" value="" shape="round" field-class="field-class"  placeholder="请输入搜索关键词"/>
			  </van-col>
			</van-row>
			
			<view  v-if="scrollTop>380" class="px">
				<view class="pxmenu">
					<view  @click="open(1)">
						<text>综合排序</text> 
					<view class="hiddenMenu" v-show="type==1">
						111111
					</view>
					</view>
					<view   ><text>销量高</text> </view>
					<view  ><text>速度快</text> </view>
					<view  ><text>津贴优惠</text> </view>
					<view  @click="open(2)"><text>筛选</text>
					 <view class="hiddenMenu" v-show="type==2">
						222222
					 </view>
					 </view>
				</view>
				
			</view>
			<!-- 遮盖 -->
			<van-overlay :show="show" @click="hide()" />
			<view class="body">
				<van-row>
				  <van-col span="24">
					  <van-search custom-class="search" input-class="input" value="" shape="round" field-class="field-class"  placeholder="请输入搜索关键词"/>
				   </van-col>
				  <van-col span="24">
					  <van-row gutter="5" >
					    <van-col span="4">
							<text class="lie">烤鳗鱼</text>
						</van-col>
					    <van-col span="5"><text class="lie">玻璃花瓶</text></van-col>
					    <van-col span="4"><text class="lie">米线</text></van-col>
						<van-col span="3"><text class="lie">炸鸡</text></van-col>
						<van-col span="3"><text class="lie">奶茶</text></van-col>
						<van-col span="5"><text class="lie">回锅肉</text></van-col>
					  </van-row>
				  </van-col>
				  <van-col span="24">
					  <swiper style="margin-top: 10px; background-color: #FFFFFF; border-radius: 20px;"indicator-dots="true" indicator-color="#FFD100" indicator-active-color="#F4F4F4">
					  	<swiper-item>
					  		<view class="daohang">
								<view >
									<view >
										<image src="../../static/icon/1.png" mode=""></image>
									</view>
									<text>精品美食</text>
								</view>
								<view >
									<view >
										<image src="../../static/icon/2.png" mode=""></image>
									</view>
									<text>超市便利</text>
								</view>
								<view >
									<view >
										<image src="../../static/icon/3.png" mode=""></image>
									</view>
									<text>蔬菜水果</text>
								</view>
								<view >
									<view >
										<image src="../../static/icon/1.png" mode=""></image>
									</view>
									<text>特价买药</text>
								</view>
								<view >
									<view >
										<image src="../../static/icon/5.png" mode=""></image>
									</view>
									<text>跑腿代购</text>
								</view>
							</view>
							<view class="daohang">
								<view >
									<view >
										<image src="../../static/icon/11.png" mode=""></image>
									</view>
									<text>甜蜜蛋糕</text>
								</view>
								<view >
									<view >
										<image src="../../static/icon/12.png" mode=""></image>
									</view>
									<text>下午饭</text>
								</view>
								<view >
									<view >
										<image src="../../static/icon/10.png" mode=""></image>
									</view>
									<text>必得好卷</text>
								</view>
								<view >
									<view >
										<image src="../../static/icon/8.png" mode=""></image>
									</view>
									<text>汉堡披萨</text>
								</view>
								<view >
									<view >
										<image src="../../static/icon/9.png" mode=""></image>
									</view>
									<text>超值联盟</text>
								</view>
							</view>
					  	</swiper-item>
					  	<swiper-item>
					  		<view class="daohang">
					  			<view >
					  				<view >
					  					<image src="../../static/icon/13.png" mode=""></image>
					  				</view>
					  				<text>休闲快餐</text>
					  			</view>
					  			<view >
					  				<view >
					  					<image src="../../static/icon/14.png" mode=""></image>
					  				</view>
					  				<text>津贴联盟</text>
					  			</view>
					  			<view >
					  				<view >
					  					<image src="../../static/icon/15.png" mode=""></image>
					  				</view>
					  				<text>美团专送</text>
					  			</view>
					  			<view >
					  				<view >
					  					<image src="../../static/icon/16.png" mode=""></image>
					  				</view>
					  				<text>日韩料理</text>
					  			</view>
					  			<view >
					  				<view >
					  					<image src="../../static/icon/17.png" mode=""></image>
					  				</view>
					  				<text>浪漫鲜花</text>
					  			</view>
					  		</view>
					  		<view class="daohang">
					  			<view >
					  				<view >
					  					<image src="../../static/icon/18.png" mode=""></image>
					  				</view>
					  				<text>麻辣小吃</text>
					  			</view>
					  			<view >
					  				<view >
					  					<image src="../../static/icon/19.png" mode=""></image>
					  				</view>
					  				<text>小吃馆</text>
					  			</view>
					  			<view >
					  				<view >
					  					<image src="../../static/icon/6.png" mode=""></image>
					  				</view>
					  				<text>肉包子</text>
					  			</view>
					  			<view >
					  				<view >
					  					<image src="../../static/icon/7.png" mode=""></image>
					  				</view>
					  				<text>营养早餐</text>
					  			</view>
					  			<view >
					  				<view >
					  					<image src="../../static/icon/20.png" mode=""></image>
					  				</view>
					  				<text>更多分类</text>
					  			</view>
					  		</view>
					  	</swiper-item>
					  </swiper>
				  </van-col>
				</van-row>
				<swiper class="hb" :autoplay="true" :interval="3000" :duration="1000" :vertical="true">
					<swiper-item>
						<view class="hbx">
							<image src="../../static/icon/hb.jpg" mode=""></image>
							<text>饭点大卡令金币</text>
							<van-button type="danger"  size="mini">去领取</van-button>
						</view>
					</swiper-item>
					<swiper-item>
						<view class="hbx">
							<image src="../../static/icon/hb.jpg" mode=""></image>
						</view>
					</swiper-item>
				</swiper>
				<swiper class="lunbo" :indicator-dots="true" :autoplay="true" :interval="3000" :duration="1000">
					<swiper-item>
						<image src="../../static/icon/a.jpg" mode=""></image>
					</swiper-item>
					<swiper-item>
						<image src="../../static/icon/b.jpg" mode=""></image>
					</swiper-item>
					<swiper-item>
						<image src="../../static/icon/d.jpg" mode=""></image>
					</swiper-item>
					<swiper-item>
						<image src="../../static/icon/e.gif" mode=""></image>
					</swiper-item>
				</swiper>
				<van-row gutter="5" v-if="scrollTop<380" class="px1">
					<van-col  span="6" ><text>综合排序</text> </van-col>
					<van-col  span="4" ><text>销量高</text> </van-col>
					<van-col  span="4" ><text>速度快</text> </van-col>
					<van-col  span="7" ><text>津贴优惠</text> </van-col>
					<van-col  span="3" ><text>筛选</text> </van-col>
				</van-row>
			</view>
		
	</view>
</template>

<script>
	var page
	// 引入SDK核心类
	var QQMapWX = require('@/modules/qqmap-wx-jssdk.js');
	 
	// 实例化API核心类
	var qqmapsdk = new QQMapWX({
	    key: 'P2RBZ-LYVW3-Z653B-Y5LPJ-VAEK2-XZBSW' // 必填
	});
	export default {
		data() {
			return {
				scrollTop: "",
				type:0,
				show:false,
				address:""
			}
		},
		onLoad() {
			page=this
			uni.getLocation({
			    type: 'wgs84',
			    success: function (res) {
			        console.log('当前位置的经度：' + res.longitude);
			        console.log('当前位置的纬度：' + res.latitude);
					 qqmapsdk.reverseGeocoder({
						 location: {
						           latitude:  res.latitude,
						           longitude: res.longitude
								   },
						success:function(res){
							console.log(res)
							page.address= res.result.formatted_addresses.recommend
						}		   
								   
					 })
			    }
			});
		},
		methods: {
			linkTo(aa){
				console.log(1111)
				uni.navigateTo({
				    url: aa
				});
			},
			open(type){
				this.show=true
				this.type=type
			},
			hide(){
				this.show=false
				this.type=0
			}
			
		},
		onPageScroll(e){
			console.log(e)
			page.scrollTop=e.scrollTop
			
		}
	}
</script>

<style>
	.cc{
		width: 750rpx;
		min-height: 70px;
		background-color: #FFD100;
		display: flex;
		align-items: center;
		font-size: 12px;
		position: fixed;
		z-index: 999;
		top: 0;
		left:0;
	}
	.cc1{
		width: 750px;
		min-height: 70px;
		background-color: #FFFFFF;
		display: flex;
		align-items: center;
		position: fixed;
		z-index: 999;
		top: 0;
		left:0;
	}
	.body{
		border: 1px solid #FFFFFF;
		margin-top: 70px;
		min-height: 200px;
		background-color: #FBFBFB;
		padding: 1px 20rpx;
		border-radius: 40rpx 40rpx 0 0;
		
		
	}
	.search{
		padding:0!important;
		margin-top: 10px;
	}
	.search2{
		padding:0!important;
		margin-top: 10px;
		width: ;
	}
	.search>view{
		padding: 0!important;
	}
	.lie{
		font-size: 12px;
		background: #e3e3e3;
		border-radius: 10px;
	}
	.input{
		background-color: #e3e3e3;
	}
	.daohang{
		padding: 8px 10px 0px 10px;
		display: flex;
		justify-content: space-between;
		
		
	}
	.daohang>view{
		   display: flex;
		   flex-flow: nowrap column;
		   align-items: center;
		   font-size: 10px;
	}
	.daohang image{
		width: 40px;
		height: 40px;
	}
	.daohang text{
		font-size: 11px;
	}
	.hb{
		background-color: #FEF8E0;
		padding: 0px 10px;
		margin-top: 10px;
		height: 30px;
		border-radius: 20px;
		min-width: 90%;
		border-radius: 10px;
	}
	.hbx{
		background-color: #FEF8E0;
		display: flex;
		justify-content: space-around;
		align-items: center;
	}
	.hbx image{
		height: 20px;
		width: 15px;
	}
	.lunbo{
		background-color: #FFFFFF;
		padding: 0px 10px;
		margin-top: 10px;
		height: 90px;
		border-radius: 20px;
		min-width: 90%;
	}
	.lunbo image{
		width: 100%;
		height: 90px;
		border-radius: 10px;
	}
	.px{
		position: fixed;
		width: 100%;
		background-color: #FFFFFF;
		position: fixed;
		top: 70px;
		left:0;
		z-index: 99;
	}
	.pxmenu{
		width: 100%;
		font-size: 11px;
		display: flex;
		justify-content: space-between;
		position: relative;
		z-index: 99;
	}
	.hiddenMenu{
		
		width: 750rpx;
		min-height: 60px;
		background-color:#FFFFFF;
		position: absolute;
	    top:100%;
		left:0px;
	
	}
	.px1{
		width: 100%;
		font-size: 11px;
		
		background-color: #FFFFFF;
		
	}
</style>
