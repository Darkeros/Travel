<template>
	<div class="icons">
		<swiper>
			<swiper-slide v-for="(page, index) in pages" :key="index">
				<div class="icon" v-for="item in page" :key="item.id">
					<div class="icon-img">
						<img class="icon-imgcontent" :src="item.imgUrl">
					</div>
					<p class="icon-desc">{{item.desc}}</p>
				</div>
			</swiper-slide>
		</swiper>
	</div>
</template>

<script>
	export default {
		name: 'HomeIcons',
		data () {
			return {
				iconList: [
				{id: '0001',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',desc: '热门景点'},
				{id: '0002',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',desc: '一日游'},
				{id: '0003',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',desc: '上海必游'},
				{id: '0004',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',desc: '游乐场'},
				{id: '0005',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',desc: '夏日玩水'},
				{id: '0006',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1805/57/1e29afd06f881102.png',desc: '普陀山'},
				{id: '0007',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png',desc: '上海欢乐谷'},
				{id: '0008',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/95/8d02011d149bdb02.png',desc: '汽车站'},
				{id: '0009',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/de/f26be47a6bf02a02.png',desc: '上海迪士尼'},
				{id: '0010',imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',desc: '全部游玩'},
				]
			}
		},
		computed: {
			pages () {
				const pages = []
				this.iconList.forEach((item, index) => {
					const page = Math.floor(index / 8)
					if(!pages[page]){
						pages[page] = []
					}
					pages[page].push(item)
				})
				return pages
			}
		}
	}
</script>

<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	@import '~styles/mixins.styl'
	.icons >>> .swiper-container
		overflow: hidden
		height: 0
		padding-bottom: 50%
	.icon
		float: left
		width: 25%
		height: 0
		padding-bottom: 25%
		position: relative
		overflow: hidden
		.icon-img
			position: absolute
			top: 0
			left: 0
			right: 0
			bottom: .44rem
			box-sizing: border-box
			padding: .1rem
			.icon-imgcontent
				height: 100%
				display: block
				margin: 0 auto
		.icon-desc
			position: absolute
			left: 0
			right: 0
			bottom: 0
			line-height: .44rem
			height: .44rem
			color: $darkTextColor
			text-align: center
			ellipsis()
</style>