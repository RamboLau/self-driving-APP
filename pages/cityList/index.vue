<template>
	<!-- 城市列表插件 -->
  <view class="demo">
    <ss-select-city :hotCitys="hotCitys" v-model="value" @on-select="onSelect"></ss-select-city>
  </view>
</template>

<script>
  import ssSelectCity from '@/components/ss-select-city/ss-select-city.vue'
  export default {
    data() {
      return {
        hotCitys: ['杭州', '天津', '北京', '上海', '深圳', '广州', '成都', '重庆', '厦门'],
        value: '杭州',
		
      }
    },
    components: {
      ssSelectCity
    },
    methods: {
      onSelect(city) {
		  this.value = city;
      }
    },
	//点击导航栏确定按钮，触发事件
	onNavigationBarButtonTap(val) {
		console.log("保存成功");
		this.$emit('target()',this.value);
		uni.redirectTo({
		    url: '/pages/offer-reward/createReward/createReward',
		    animationType: 'pop-in',
		    animationDuration: 200
		});
	}
  }
</script>

<style lang="scss" scoped>

</style>

