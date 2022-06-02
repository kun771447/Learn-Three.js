![](D:\Web\Three.js\assets\2022-06-02-11-39-10-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-39-29-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-40-09-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-41-00-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-41-20-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-41-41-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-41-55-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-42-10-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-42-53-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-43-21-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-44-27-image.png)

 ![](D:\Web\Three.js\assets\2022-06-02-11-44-38-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-46-54-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-47-59-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-49-33-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-49-46-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-51-12-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-52-06-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-54-31-image.png)

![](D:\Web\Three.js\assets\2022-06-02-11-54-48-image.png)

## 四大组建

#### 1. 场景

场景就是舞台，你可以把任何要显示的东西，放在场景中的任何位置

THREE.Scene = function() {}

![](D:\Web\Three.js\assets\2022-05-30-16-16-42-image.png)

### 2. 相机

相机就是现实生活中的相机，我们最终能够在浏览器中看到的景象，就是相机拍摄出来

#### ![](D:\Web\Three.js\assets\2022-05-30-16-18-49-image.png)

#### 两大相机

![](D:\Web\Three.js\assets\2022-05-30-16-18-59-image.png)

透视相机：透视投影，即离视点近大远小，远道极点即为消失，成为灭点

正投影相机：远处和近处的一样大

相机参数
THREE.PerspectiveCamera = function(fov, aspect, near, far)

![](D:\Web\Three.js\assets\2022-05-30-16-20-05-image.png)

### ![](http://www.hewebgl.com/attached/image/20130530/20130530151418_279.jpg)

- 1、视角fov：这个最难理解,我的理解是,眼睛睁开的角度,即,视角的大小,如果设置为0,相当你闭上眼睛了,所以什么也看不到,如果为180,那么可以认为你的视界很广阔,但是在180度的时候，往往物体很小，因为他在你的整个可视区域中的比例变小了

- 2、近平面near：这个呢，表示你近处的裁面的距离。补充一下，也可以认为是眼睛距离近处的距离，假设为10米远，请不要设置为负值，Three.js就傻了,不知道怎么算了,

- 3、远平面far：这个呢，表示你远处的裁面,

- 4、纵横比aspect：实际窗口的纵横比，即宽度除以高度。这个值越大，说明你宽度越大，那么你可能看的是宽银幕电影了，如果这个值小于1，那么可能你看到的是如下的图中的LED屏幕了

- ![](http://www.hewebgl.com/attached/image/20130530/20130530152221_826.jpg)

```js
var camera = new THREE.PerspectiveCamera( 45, width / height, 1, 1000 );

scene.add( camera );
```

### 3. 渲染器

渲染器,决定了画家怎么将眼前的场景画到屏幕上。渲染即 THREE.WebGLRenderer()

### 4. 几何体

![](D:\Web\Three.js\assets\2022-05-30-16-32-36-image.png)