<template>
	<div class="header">
		<div class="header-left">
			<div class="iconfont back-icon">&#xe624;</div>
		</div>
		<div class="header-input">
			<span class="iconfont">&#xe632;</span>
			输入城市景点/游玩主题
		</div>
		<div class="header-right">
			<span class="iconfont arrow-icon">&#xe65e;</span>
			城市
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Home'
	}
</script>

<style lang=stylus scoped>
@import '~styles/varibles.styl'
.header
	line-height: .86rem
	display: flex
	background: $bgColor
	color: #fff
	.header-left
		width: .64rem
		float: left
		.back-icon
			text-align: center
			font-size: .4rem
	.header-input
		flex: 1
		height: .64rem
		margin-top: .12rem
		margin-left: .2rem
		background: #fff
		border-radius: .1rem
		color: #ccc
		line-height: .64rem
		height: .64rem
		padding-left: .1rem
	.header-right
		width: 1.24rem
		float: right
		text-align: center
		.arrow-icon
			font-size: .24rem
			margin-right: -.05rem
</style>