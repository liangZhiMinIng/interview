###### 移动APP

1. 首页轮播图如何实现？
   - 将antd-vue中的carousel(木马)导入到项目，按照官网的例子进行编写。
   - 现在引用这个carousel会报错，是因为浏览器的安全机制passive导致的。
   - 将图片引入到轮播图中
2. 商品卡片滚动如何实现？
   - 创建商品卡片组件
   - 使用css实现滚动
     - 设置父元素的样式
       - .product-list {
             display:flex;         /* 让子元素显示在一行 */
             overflow-x: auto;     /* !!! 横向的overflow设置为auto */
             margin-top:18px;
             padding:2px;
             box-sizing: border-box;
         }
     - 设置子元素的样式
       - .product-item {
             flex-shrink:0;        /* 保证子元素的长宽比例不改变 */
             margin-right:15px;
         }
   - 使用第三方库实现横向滚动  better-scroll
   - 总结：better-scroll实现的效果细节比自己用css实现的好，例如回弹的效果
3. 搜索框过滤如何实现？
4. 实现类别页面，使用的是沉浸式布局

