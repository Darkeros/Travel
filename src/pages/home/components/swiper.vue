<template>
	<div class="weapper">
		<swiper :options="swiperOption">
		    <swiper-slide v-for="item in swiperList" :key="item.id">
		    	<img class="swiper-img" :src="item.imgUrl">
		    </swiper-slide>
		    <div class="swiper-pagination"  slot="pagination"></div>
		</swiper>
	</div>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		data () {
			return {
				swiperOption: {
					pagination: '.swiper-pagination',
					loop: true
				},
				swiperList: [{
					id: '0001',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/ad/1d2e0030d4ff7302.jpg_750x200_bf5a325d.jpg'
				},{
					id: '0002',
					imgUrl: 'http://img1.qunarzz.com/piao/fusion/1808/16/074e0e717c92a602.jpg_750x200_37ec9a1b.jpg'
				}]
			}
		}
	}
</script>

<style lang="stylus" scoped>
	.weapper >>> .swiper-pagination-bullet-active
		background-color: #fff !important
	.weapper
		width: 100%
		height: 0
		overflow: hidden
		padding-bottom: 31.25%
		background-color: #eee
		.swiper-img
			width: 100%
</style>