<template>
	<div class="header">
		<div class="header-left">
			<div class="iconfont back-icon">&#xe624;</div>
		</div>
		<div class="header-input">
			&nbsp;
			<span class="iconfont">&#xe632;</span>
			&nbsp;输入城市/景点/游玩主题</div>
		<router-link to='/city'>
			<div class="header-right">
				{{this.city}}
				<span class="iconfont arrow-icon">&#xe615;</span>
			</div>
		</router-link>
	</div>
</template>

<script>
import {mapState} from 'vuex'
export default {
	name: 'HomeHeader',
	computed: {
		...mapState(['city'])
	}
}
</script>

<style lang="stylus" scoped>
	@import '~styles/varibles.styl'
	.header
		display: flex
		line-height: $headerHeight
		background: $bgColor
		color: #fff
		.header-left
			width: .64rem
			float: left
			.back-icon
				text-align: center
				font-size: .2rem
		.header-input
			flex: 1
			height: .64rem
			margin-top: .12rem
			margin-left: .2rem
			padding-left: .2rem
			background: #fff
			border-radius: .1rem
			color: #ccc
			line-height: .64rem
		.header-right
			color: #fff
			min-width: 1.04rem
			padding: 0 .1rem
			float: right
			text-align: center
			.arrow-icon
				margin-left: -.04rem
				font-size: .2rem
</style>
