<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
		    <swiper-slide v-for="item of swiperList" :key="item.id">
		    	<img class="swiper-img" :src="item.imgUrl" />
		    </swiper-slide>
		    <div class="swiper-pagination"  slot="pagination"></div>
	    </swiper>
    </div>
</template>

<script>
export default {
	name: 'HomeSwiper',
	data: function() {
		return {
			swiperOption: {
				pagination: '.swiper-pagination',
				loop: true
			},
			swiperList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/39/6b1f0402bb1d5902.jpg_750x200_3c7661d6.jpg'
			}, {
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/piao/fusion/1812/a8/90d66a621daf6802.jpg_750x200_d479b789.jpg'
			}]
		}
	}
}
</script>

<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
		background: #fff
	.wrapper
		overflow: hidden
		width: 100%
		height: 0
		padding-bottom: 31%
		.swiper-img
			width: 100%
		
</style>