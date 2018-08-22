<template>
	<div class="">
		<div class="title">周末去哪</div>
		<ul>
			<li class="item border-bottom" v-for="item in recommentList" :key="item.id">
				<div class="item-img-wrapper">
					<img class="item-img" :src="item.imgUrl">
				</div>
				
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: 'HomeRecommend',
		data () {
			return {
				recommentList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
				title: '上海大康水上乐园',
				desc: '中西合璧，现代和传统各有各的精彩'
			},{
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
				title: '上海大康水上乐园',
				desc: '中西合璧，现代和传统各有各的精彩'
			},{
				id: '0003',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
				title: '上海大康水上乐园',
				desc: '中西合璧，现代和传统各有各的精彩'
			}]
			}
		}
	}
</script>

<style lang="stylus" scoped>
	@import '~styles/mixins.styl'
	.title
		margin-top: .2rem
		line-height: .8rem
		background: #eee
		text-indent: .2rem
	.item-img-wrapper
		height: 0
		overflow: hidden
		padding-bottom: 33.9%
	.item-img
		width: 100%
	.item-info
		padding: .1rem
		.item-title
			line-height: .4rem
			font-size: .32rem
			ellipsis()
		.item-desc
			line-height: .4rem
			color: #ccc
			ellipsis()
</style>