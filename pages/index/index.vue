<template>
  <view class="container">
	<button @click="connectService" type="primary">初始化连接</button>
    <button @click="getResult1" type="primary">原获取称重信息</button>
	<button @click="getResult2" type="primary">获取称重信息</button>
    <button @click="getStatus" type="primary">获取称重状态</button>
    <button @click="getPrice" type="primary">获取计价结果</button>
	<button @click="zero" type="primary">清零</button>
	<button @click="tare" type="primary">去皮</button>
  </view>
</template>

<script>
const electronic = uni.requireNativePlugin('electronic');

export default {
  data() {
    return {};
  },
  methods: {
		connectService() {
			electronic.connectService(
			e => {
				uni.showToast({
					title:JSON.stringify(e),
					icon:"none"
				})
			}
			)
		},
		getResult1() {
		  electronic.getResult(
		  e => {
		  	uni.showToast({
		  		title:JSON.stringify(e),
		  		icon:"none"
		  	})
		  }
		  )
		},
		getResult2() {
		  electronic.getRData(
		  e => {
		  	uni.showToast({
		  		title:JSON.stringify(e),
		  		icon:"none"
		  	})
		  }
		  )
		},
		getStatus() {
		  electronic.getStatus(
		  e => {
		  	uni.showToast({
		  		title:JSON.stringify(e),
		  		icon:"none"
		  	})
		  })
		},
		getPrice() {
		  electronic.getPrice(
		  e => {
		  	uni.showToast({
		  		title:JSON.stringify(e),
		  		icon:"none"
		  	})
		  })
		},
		zero() {
		  electronic.zero(
		  e => {
		  	uni.showToast({
		  		title:JSON.stringify(e),
		  		icon:"none"
		  	})
		  })
		},
		tare() {
		  electronic.tare(
		  e => {
		  	uni.showToast({
		  		title:JSON.stringify(e),
		  		icon:"none"
		  	})
		  })
		},
  },
};
</script>

<style>
.container {
  padding: 20px;
  font-size: 14px;
  line-height: 24px;
}
</style>
