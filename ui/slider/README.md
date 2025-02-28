# Slider

## 介绍

轮播组件，主要使用场景有网页中的运营广告。scroller、tab、slider 组件皆使用 Slide.js，源码修改自 IScroll。下载地址：https://github.com/hahnzhu/slide.js

## 调用方式

HTML 示意：
```
<div class="ui-slider">
	<ul class="ui-slider-content">
		<li>热门推荐</li>
        <li>限时免费</li>
        <li>全部表情</li>
    </ul>
    <ul class="ui-slider-indicators">
    	<li class="current">1</li>
    	<li>2</li>
    	<li>3</li>
    </ul>
</div>
```

组件初始化的时候需要传入 wrapper ('.ui-slider')。实际滚动的是内部的 scroller ('.ui-slider-content')。因为样式结合了 Frozen UI，所以类名固定。如需其它样式可自行覆盖。

```js
window.addEventListener('load', function(){
	
	var slider = new Slide('.ui-slider', {
		role: 'slider',
		indicator: true,
		autoplay: true,
		interval: 3000
	});

	/* 滑动开始前 */
	slider.on('slideStart', function() {
	})

	/* 滑动结束 */
	slider.on('slideEnd', function() {
	})

})
</script>
```


## 配置说明

<table>
	<tr>
		<th>name</th>
		<th>type</th>
		<th>default</th>
		<th>description</th>
	</tr>
	<tr>
		<td>role</td>
		<td>string</td>
		<td>''</td>
		<td>角色(slider、tab)</td>
	</tr>
	<tr>
		<td>indicator</td>
		<td>boolean</td>
		<td>true</td>
		<td>指示点</td>
	</tr>
	<tr>
		<td>autopaly</td>
		<td>boolean</td>
		<td>false</td>
		<td>自动播放</td>
	</tr>
	<tr>
		<td>interval</td>
		<td>int</td>
		<td>2000</td>
		<td>自动播放间隔时间</td>
	</tr>
	<tr>
		<td>slideStart</td>
		<td>function</td>
		<td>function(){}</td>
		<td>滑动开始前调用</td>
	</tr>
	<tr>
		<td>slideEnd</td>
		<td>function</td>
		<td>function(){}</td>
		<td>滑动结束时调用</td>
	</tr>
</table>

