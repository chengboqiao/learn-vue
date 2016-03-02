# learn-vue
使用vue.js搭建个人网站
#####使用技术： vue.js+webpack
#####项目说明： 此项目是本人空余时间搭建的，项目会一直迭代更新。希望大家提供宝贵的意见和建议，谢谢。
#####邮&emsp;&emsp;&ensp;箱： yin_x_f@163.com
#####个人网站： http://www.coderyin.com/
#####个人博客： http://www.jianshu.com/users/489e597a9cad/latest_articles


####历史更新
  *2016.03.02*

  1.修改博客首页，数据从.json文件读取，嵌套页面数据;

     注意点：绑定图片src应该这么写：<img v-bind:src=item.img alt="文章图片">（不加{{}}），不推荐src={{item.img}}

  *2016.03.01*
  
  1.增加博客版块页面;

  2.修改webpack配置文件webpack.config.js,以支持编译多个对应的js文件;
     
     原先：
     
     entry: './src/app.js',
     output: {
      path: './dist', //文件夹生成的目录
      publicPath: '../dist/', //静态文件（图片）的路径
      filename: 'app.js'
    },
    
    新的：
    entry: {
      app:['./src/app.js'],
      blog_index:['./src/blog_index.js']
    },
    output: {
      path: './dist', //文件夹生成的目录
      publicPath: '../dist/', //静态文件（图片）的路径
      filename: '[name].js'
    }
 
  3.博客版块json文件添加；
  
  *2016.02.26*
  
  	1. 增加页面跳转，url传参;
  	2. 增加get请求，模拟请求本地json文件，获得数据，重设数据源;
  	3. 添加公用方法库——utils.js,其中添加自定义方法获取浏览器地址栏参数;
  	4. 在组件中增加引用第三方库：jquery.highcharts,并完成页面操作;
  
  *2016.02.25*

  	1. 初始化项目搭建;
