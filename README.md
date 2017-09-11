## weixinAudio.js 

####一个简单的微信样式播放器

播放器DOM及CSS是微信里内置的音频播放器的样式，重新创建了控制层js，方便在在公众号，APP等场景使用。

### 截图

![](https://ws3.sinaimg.cn/large/006tKfTcly1fjfxrz92djg30bo02jwzk.gif)

### 如何使用

通过以下demo来实现

### HTML模板

```
<p class="weixinAudo">
	<audio src="../sound/sound1.mp3" id="media" width="1" height="1" preload></audio>
	<span id="audio_area" class="db audio_area">
		<span class="audio_wrp db">
			<span class="audio_play_area">
				<i class="icon_audio_default"></i>
				<i class="icon_audio_playing"></i>
            </span>
			<span id="audio_length" class="audio_length tips_global">3:07</span>
			<span class="db audio_info_area">
                <strong class="db audio_title">标题1</strong>
                <span class="audio_source tips_global">来源1</span>
			</span>
			<span id="audio_progress" class="progress_bar" style="width: 0%;"></span>
	 	</span>
	</span>
</p>
<!-- 也可以多音频使用 -->
<!-- 注意使用同一类名，在js中进行初始化 -->
<p class="weixinAudo">
  <audio src="../sound/sound2.mp3" id="media" width="1" height="1" preload></audio>
  <span id="audio_area" class="db audio_area">
    <span class="audio_wrp db">
      <span class="audio_play_area">
        <i class="icon_audio_default"></i>
        <i class="icon_audio_playing"></i>
            </span>
      <span id="audio_length" class="audio_length tips_global">3:07</span>
      <span class="db audio_info_area">
                <strong class="db audio_title">标题2</strong>
                <span class="audio_source tips_global">来源2</span>
      </span>
      <span id="audio_progress" class="progress_bar" style="width: 0%;"></span>
    </span>
  </span>
</p>
```

### Js调用

```
//你需要先引入一个jQuery
<script src="http://libs.baidu.com/jquery/2.0.0/jquery.min.js"></script>
<script src="js/weixinAudio.js"></script>
<script>
   $('.weixinAudo').weixinAudio(options);
</script>
```
