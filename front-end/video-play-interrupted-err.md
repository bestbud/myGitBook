# 调用video.play()报错

调用`videoElem.play()`有时会产生异常：

**DOMException: The play() request was interrupted by a call to pause(). **



https://goo.gl/LdLk22 已说明这类异常产生的原因:

调用play开始加载媒体内容时被打断，play为异步调用，返回promise



### 中断的原因有两种：

 - 调用video.pause()

 - 调用video.load(), video.src或video.srcObject重新复制导致播放状态被重置



### 针对第一种情况的修复：

```

video.play().then(() => {

    video.pause()

}).catch((e) => {console.error(e)})

```

### 针对第二种情况：

```

   video.addEventListener('canplay', () => {

     video.play().then(() => {

        console.log('play  success')

      }).catch((err) => {

       console.error('play err', err)

      })

    }, { once: true })

   video.src = newSrc

```