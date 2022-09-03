# HTML多媒体
## 图片 
**原则：** 如果图像对您的内容里有意义，则应使用 HTML 图像。如果图像纯粹是装饰，则应使用 CSS 背景图片。

`<img>`元素 `<img src(source)="相对路径/绝对URL">`

**例如1：** `<img src="images/haijing.jpg">` 相对路径√
**补充：** 搜索引擎也读取图像的文件名并把它们计入 SEO，为了便于被搜索，图片需要有个描述性的文件名，而不是乱码。
**例如2：** `<img src="https://www.example.com/images/dinosaur.jpg">` 绝对路径× 
**补充：** 绝对路径图片不受控或被原网页替换，图片的版权容易引发事故
### 图片元素的属性
**alt:** 对图片的文字描述,当图片无法显示或无法被读者看到时，可以借由此了解图片内容，以免错失信息。因此，装饰性的图片用css实现，不要放在html文件里。
><img src="images/dinosaur.jpg" alt="The head and torso of a dinosaur skeleton;it has a large head with long sharp teeth">
**width与height：** 图片的宽度与高度
><img src="images/dinosaur.jpg" alt="一只恐龙头部和躯干的骨架，它有一个巨大的头，长着锋利的牙齿。" width="400" height="341">
**title：** 鼠标悬停提示，意义不大
><img src="images/dinosaur.jpg" 
alt="一只恐龙头部和躯干的骨架，它有一个巨大的头，长着锋利的牙齿。"
width="400" height="341" 
title="A T-Rex on display in the Manchester University Museum">

**figure与figcaption：** 为图片提供一个语义容器，在说明（不一定是文本，可以是其他图片、音视频、表格等）和图片间建立清晰关联。
<figure>
  <img src="https://raw.githubusercontent.com/mdn/learning-area/master/html/multimedia-and-embedding/images-in-html/dinosaur_small.jpg"
      alt="一只恐龙头部和躯干的骨架，它有一个巨大的头，长着锋利的牙齿。"
      width="400"
      height="341">
  <figcaption>曼彻斯特大学博物馆展出的一只霸王龙的化石</figcaption>
</figure>