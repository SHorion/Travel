<template>
	<div>
		<div class="title">周末热销</div>
		<ul>
			<li class="item" v-for="item of weekendList" :key="item.id">
				<div class="item-img-wrapper">
					<img class="item-img" :src="item.imgUrl" />
				</div>
				<div class="item-info">
					<p class="item-name">{{ item.name }}</p>
					<p class="item-desc">{{ item.desc }}</p>
				</div>
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	name: 'HomeWeekend',
	data () {
		return {
			weekendList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
				name: '京城人的周末撒欢地',
				desc: '在帝都过周末，不仅仅是城中游！'
			}, {
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1811/7e/476589267ebb41.jpg_r_640x214_bf599709.jpg',
				name: '京城欢乐亲子游',
				desc: '德智体美劳全面发展的亲子日，这些地方该去看看…'
			}, {
				id: '0003',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg',
				name: '京城有好泉',
				desc: '细数北京温泉，温暖你的冬天'
			}, {
				id: '0004',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1505/aa/7baaf8a851d221.jpg_r_640x214_1431200f.jpg',
				name: '北京必游TOP10',
				desc: '来北京必去的景点非这些地方莫属'
			}, {
				id: '0005',
				imgUrl: 'http://img1.qunarzz.com/sight/source/1505/9e/21df651e19af5d.jpg_r_640x214_3ea5bb38.jpg',
				name: '寻找北京的皇城范儿',
				desc: '数百年的宫廷庙宇，至今依旧威严霸气'
			},]
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
		overflow: hidden
		height: 0
		padding-bottom: 33.9%
		.item-img
			width: 100%
	.item-info
		flex: 1
		padding: .1rem
		.item-name
			line-height: .54rem
			font-size: .32rem
			ellipsis()
		.item-desc
			line-height: .4rem
			color: #ccc
			ellipsis()
</style>