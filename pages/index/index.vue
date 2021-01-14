<template>
	<view class="content">
		<goUpNotice :list="goUpNoticeList" :themeColor="themeColor"></goUpNotice>

	</view>
</template>

<script>
	import goUpNotice from '@/components/notice-goUp/notice-goUp.vue';
	export default {
		components: {
			goUpNotice,

		},
		data() {
			return {
				themeColor: '#33CCCC',
				goUpNoticeList: [{
						directOne1: '路遥知马力，日久见人心',
						directOne2: '《元曲选·争报恩》',
					}, {
						directOne1: '天生我材必有用',
						directOne2: '李白',
					},
					{
						directOne1: '穷则独善其身，达则兼济天下',
						directOne2: '孟子',
					}, {
						directOne1: '业精于勤，荒于嬉；行成于思，毁于随',
						directOne2: '韩愈',
					}, {
						directOne1: '一年之计在于春，一日之计在于晨',
						directOne2: '萧绎',
					},
				]
			}
		},
		onLoad() {
			let that = this;

		},

		methods: {
			onSelected(res) {
				//[[{"text":"<1折","value":"0.9","select":true}],[{"text":"距离优先","value":"距离优先","select":true}]]
				// console.log('res  ' + JSON.stringify(res))
				// console.log('res  ' + JSON.stringify(res[0]))
				// console.log('res  ' + JSON.stringify(res[0][0].value))
				let that = this;
				let one = res[0][0].value;
				let two = res[1][0].value;
				console.log(' one ' + one + ' two ' + two);


			},

		}
	}
</script>

<style>
	/* page {
		background-color: #f2f2f2;
	} */
</style>
