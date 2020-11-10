<template>
	<view>
		这里是地图
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
				
			}
		},
		onLoad(){
			page=this
			uni.getLocation({
			    type: 'gcj02', //返回可以用于uni.openLocation的经纬度
			    success: function (res) {
			        const latitude = res.latitude;
			        const longitude = res.longitude;
			        uni.openLocation({
			            latitude: latitude,
			            longitude: longitude,
			            success: function () {
			                console.log('success');
			            }
			        });
			    }
			});
			
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
