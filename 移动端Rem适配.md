### 移动端适配
- web页面跑在手机端（h5页面）
- 跨平台
- 基于webview（）
- 基于webkit

#### 常见适配方法
- pc端采用display：inline-block，让div盒子横着排
- 移动web：采用定高，宽度百分比，**flex弹性布局**，meDIA QUERY **媒体查询**；

- **媒体查询**
  结合css，通过媒体类型（screen、print）和媒体参数（max-width）
      
       @media screen and (max-width: 320px){
            /* css在屏幕跨度<=320px时这段样式生效 */
            .inner{
                float: left;
            }
        }
        @media screen and (min-width: 321px){
            .inner{
            }
        }

以上实现了一个简单的横排和竖排的响应

- **rem原理**与简介
Rem就是一个字体单位，类似于px，
**区别：**他会根据HTML根元素大小而定，同时也可以作为高度和宽度的单位。
**适配原理**：动态修改html的font-size适配；rem是通过不同屏幕的大小设置html根元素的font-size的属性大小来实现适配。

        /* +_media实现*/
        @media screen and (max-width: 360px) and (min-width: 321px){
            html{
                font-size: 20px;
            }
        }
        @media screen and (max-width: 320px){
            html{
                font-size: 24px;
            }
        }

通过JS动态设置font-size：

	//获取视窗宽度
    let htmlWidth = document.documentElement.clientWidth || document.body.clientWidth;
	        console.log(htmlWidth);
     let htmlDom = document.getElementsByTagName('html')[0];
	        htmlDom.style.fontSize = htmlWidth/10 + 'px';

##### rem进阶
- rem基准值计算

    1rem = 16px
- rem数值计算与构建

    170/16 = 170px
- rem与scss结合使用（node-sass安装）
  也可以直接安装sass（安装教程http://www.cnblogs.com/yehui-mmd/p/8035170.html）
- rem适配实战
通过监听浏览器视口来进行适配

	let htmlDom = document.getElementsByTagName('html')[0];
	window.addEventListener('resize', (e)=>{
	    //获取视窗宽度
	    let htmlWidth = document.documentElement.clientWidth || document.body.clientWidth;
	    htmlDom.style.fontSize = htmlWidth/10 + 'px';
	})
	
定义rem适配的函数及使用（sass语法）

	@function px2rem($px) {
	    $rem:37.5px;//iphone6
	    @return ($px / $rem) + rem;
	}
	.header{
	    width:100%;
	    height: px2rem(40px);
	    background-color: red;
	    padding-left: px2rem(23px);
	 }