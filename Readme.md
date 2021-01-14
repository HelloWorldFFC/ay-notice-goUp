
## 前言
简介：消息通知动态往上翻，类似支付宝首页消息通知，传入数据即可使用

## 有疑问
微信搜索“慢慢向好”小程序，找客服反馈，相应问题。
				  

## 素材
[图片资源](https://pixabay.com)
 
## 开始使用
下载源码解压，复制`/components` 下的组件至项目根目录的 `/components` 文件夹下


`index.vue`的`script`加入如下部分：
```
import goUpNotice from '@/components/notice-goUp/notice-goUp.vue';

components: { goUpNotice },

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
```


`index.vue`的`template`加入如下部分：
```
<goUpNotice :list="goUpNoticeList" :themeColor="themeColor"></goUpNotice>

```

引入阿里矢量图，复制示例源码`/style` 下的`/iconfont.css`至项目根目录的 `/style` 文件夹下，内容如下：

```
@font-face {font-family: "iconfont";
  src: url('//at.alicdn.com/t/font_2190080_glfs1acu1yq.eot?t=1607330521015'); /* IE9 */
  src: url('//at.alicdn.com/t/font_2190080_glfs1acu1yq.eot?t=1607330521015#iefix') format('embedded-opentype'), /* IE6-IE8 */
  url('data:application/x-font-woff2;charset=utf-8;base64,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') format('woff2'),
  url('//at.alicdn.com/t/font_2190080_glfs1acu1yq.woff?t=1607330521015') format('woff'),
  url('//at.alicdn.com/t/font_2190080_glfs1acu1yq.ttf?t=1607330521015') format('truetype'), /* chrome, firefox, opera, Safari, Android, iOS 4.2+ */
  url('//at.alicdn.com/t/font_2190080_glfs1acu1yq.svg?t=1607330521015#iconfont') format('svg'); /* iOS 4.1- */
}

.iconfont {
  font-family: "iconfont" !important;
  font-size: 16px;
  font-style: normal;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.icon-shang3:before {
  content: "\e689";
}

.icon-xia:before {
  content: "\e65a";
}

.icon-you:before {
  content: "\e600";
}

.icon-tubiaozhizuo-:before {
  content: "\e605";
}

.icon-time:before {
  content: "\e619";
}

.icon-xiaoxi:before {
  content: "\e615";
}

.icon-daohangdizhi:before {
  content: "\e65e";
}

.icon-gouxuan:before {
  content: "\e6ce";
}

.icon-icon_fuben:before {
  content: "\e611";
}

```


页面`App.vue` 引入css
```
<style>
	/*每个页面公共css */
	@import './style/iconfont.css';
</style>
```

 