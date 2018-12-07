<template>
	<div>
		<div class="title">热销推荐</div>
		<ul>
			<li class="item" v-for="item of recommendList" :key="item.id">
				<div class="item-img-wrapper">
					<img class="item-img" :src="item.imgUrl" />
				</div>
				<div class="item-info">
					<p class="item-title">{{ item.title }}</p>
					<p class="item-desc">{{ item.desc }}</p>
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
			recommendList: [{
				id: '0001',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
				title: '故宫',
				desc: '海淀区'
			}, {
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1711/53/53f7752ece875d00a3.img.jpg_200x200_5c006913.jpg',
				title: '龙脉温泉',
				desc: '昌平区'
			}, {
				id: '0003',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1709/e4/e48857f2ce5e53a7a3.img.jpg_200x200_8ee069fe.jpg',
				title: '远去的恐龙',
				desc: '朝阳区'
			}, {
				id: '0004',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1602/67/67feeab24cfc82bb90.water.jpg_200x200_af2a01b1.jpg',
				title: '太平洋海底世界',
				desc: '海淀区'
			}, {
				id: '0005',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/43/dea8b51719a4a69b68777baa68c146e4.water.jpg_200x200_8da8cebe.jpg',
				title: '春晖园温泉度假村春晖园温泉度假村',
				desc: '顺义区'
			}, {
				id: '0006',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/1708/2b/2b3b94de99c0a425a3.img.jpg_200x200_2458ffb2.jpg',
				title: '八达岭长城',
				desc: '延庆县'
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
			padding: .1rem
			min-width: 0
			.item-title
				line-height: .54rem
				font-size: .32rem
				ellipsis()
			.item-desc
				line-height: .4rem
				color: #ccc
				ellipsis()
			.item-button
				line-height: .44rem
				margin-top: .16rem
				background: #ff9300
				padding: 0 .1rem
				border-radius: .06rem
				color: #fff
</style>