<template>
	<div class="">
		<div class="title">热销推荐</div>
		<ul>
			<li class="item border-bottom" v-for="item in recommentList" :key="item.id">
				<img class="item-img" :src="item.imgUrl">
				<div class="item-info">
					<p class="item-title">{{item.title}}</p>
					<p class="item-desc">{{item.desc}}</p>
					<button class="item-button">查看详情</button>
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
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
				title: '上海大康水上乐园',
				desc: '中西合璧，现代和传统各有各的精彩'
			},{
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
				title: '上海大康水上乐园',
				desc: '中西合璧，现代和传统各有各的精彩'
			},{
				id: '0003',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
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
	.item
		overflow: hidden
		display: flex
		height: 1.9rem
		.item-img
			width: 1.7rem
			height: 1.7rem
			padding: .1rem
		.item-info
			flex: 1
			min-width: 0
			.item-title
				line-height: .4rem
				font-size: .32rem
				ellipsis()
			.item-desc
				line-height: .4rem
				color: #ccc
				ellipsis()
			.item-button
				line-height: .4rem
				background-color: #ff9300
				padding: 0 .2rem
				border-radius: .06rem
				margin-top: .4rem
				color: #fff
</style>