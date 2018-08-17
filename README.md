Welcome
===========

qrencode -t png -o yudianr.png -s 8 https://yudianr.github.io

主题使用Litten制作的[yilia](http://litten.me/2014/08/31/hexo-theme-yilia/)
主题更新: `git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia`

```
在github页面创建分支hexo
将hexo分支克隆到本地：git clone -b hexo https://github.com/yudianr/yudianr.github.io.git
git add .
git commit -m "xxx"
git push origin hexo
```

## 相册的样式文件存放地址：./source/photos/(小图路径：./min_photos， 大图路径：./photos)
- 修改ins.js文件的render()函数，该函数式用来渲染数据，里面配置了展示图片的链接地址(minSrc & src)，图片路径规则为：https://github.com/用户名/项目名/raw/分支名/存放图片的文件夹/该文件夹下的图片，如：https://github.com/yudianr/yudianr.github.io/raw/hexo/photos/2018-07-10_湖人总冠军.jpg，浏览器也会显示为：https://raw.githubusercontent.com/yudianr/yudianr.github.io/hexo/photos/2018-07-10_湖人总冠军.jpg
- 图片处理的python脚本(tool.py  ImageProcess.py)    `./tool.py`
- 裁剪图片(cut_by_ratio):去图片的中间部分，裁剪为正方形
- 压缩图片(compress):把图片进行压缩，方便相册的加载
- 将处理后的图片(大图+小图)提交到github上(git_operation)
- 将图片信息处理成json数据格式(handle_photo):采用的方式是读取图片的名字作为其中的text的内容，图片的命名为"最前面是日期，然后用_进行分隔，后面是图片的描述信息，注意不要包含_和.符号"，json文件保存在source/photos/data.json

Reference
===========
- http://litten.me <br><br>
- http://luojh.me/ <br><br>
- http://luojh.me/2018/01/28/blog2/ <br><br>
- http://luckykun.com/ <br><br>
- http://lawlite.me/ <br><br>
