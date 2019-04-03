# 欢迎使用多端画廊组件(ynGallery)

@(组件)[画廊|影讯|图展|滑动|grally|Swiper|vue|uni-app|]

**画廊组件ynGrally**是一款在UNI-APP上开发的多端通用图片展示组件，支持调节画廊高度，图片高宽，背景过渡色，定义角标，描述，背景融合过渡,流畅的滑动感！体验感不错。

![enter image description here](https://github.com/UserWenxin/ynGallery-for-uniapp/blob/master/imgs/7.gif?raw=true)

这是微信开发工具上的gif截图(由于gif 200多色的限制，背景看起来光晕，其实很平滑的)

### 使用

下载的组件包内components目录下内含2个组件：

 一个是`ynGallery.vue`画廊组件，另一个是三角角标组件`ynTriangleBadge.vue`

  放到你可以引用的地方，例如我放在`components/YnComponents `下面 
 
然后`<script>`处引用

         import ynGallery from 'components/YnComponents/ynGallery/ynGallery.vue
         
##### 接着注册   
         components: {	
			ynGallery
		     }

##### 调用
      <ynGallery :images="testimgs" ></ynGallery> 
      
      其中示例数组testimg格式：
      	testimgs :[{url:"你的图片地址"},
		   {url:"你的图片地址2"},
		    ...]  

##### 将显示：
      
![enter image description here](https://github.com/UserWenxin/ynGallery-for-uniapp/blob/master/imgs/5.png?raw=true)



##### 单调了点，我们加上一些参数，先上效果图！

![enter image description here](https://github.com/UserWenxin/ynGallery-for-uniapp/blob/master/imgs/6.png?raw=true)

![enter image description here](https://github.com/UserWenxin/ynGallery-for-uniapp/blob/master/imgs/3.png?raw=true)
     
![enter image description here](https://github.com/UserWenxin/ynGallery-for-uniapp/blob/master/imgs/1.png?raw=true)

![enter image description here](https://github.com/UserWenxin/ynGallery-for-uniapp/blob/master/imgs/2.png?raw=true)
     
### ynGallery参数列表

| 参数           |类型    |  默认值   | 说明    |
| :--------     |------  | --------:| :--:    |
| galleryheight |Number  | 165      |  画廊高度 单位px |
| imgviewwidth  |Number  | 85       |  图片框宽度 单位px|
| imgviewheight |Number  | 105      |  图片框高度 单位px|
| bkstart       |String  | `#000000`|  背景起始色|
| bkend         |String  | `#000000`|  背景终止色|
| showbadge     |Boolean | false    |  是否显示角标|
| badegtype     |String  | trian    |  角标类型 round:圆角类型 trian:三角类型|
| badegwidth    |Number  | 25       |  角标宽度 （仅仅对三角角标有效）单位px|
| badegheight   |Number  | 25       |  角标高度 （仅仅对三角角标有效）单位px|
| showdec       |Boolean | false    |  是否显示描述|
| images        |Object  |          |  图源数组对象，结构看下面说明      |

##### images图源数组单一对象结构：		 
              imgobj:{dec:'',                   //图像描述信息
		      badeg:'',                 //角标文字
		      badegcolor:'#000000',     //角标颜色
		      url:'',                   //图源  
		      dominant:''               //主色  
		      }    

##### 按默认值调用代码示例 
	<ynGallery  					          
		  :galleryheight="165" 
		   bkstart="#000000"                     
		   bkend="#000000" 							  
		  :imgviewwidth="85" 
		  :imgviewheight="105"
		  :showbadge="true"
		   badegtype="trian"
		   badegwidth="25"
		   badegheight="25"
		  :showdec="true"
		  :images="testimgs" 
		  @clickimg="onclickimg"
		  >   
	</ynGallery>

##### 事件
    名称：clickimg：  
    参数：clickimg(imgviewobj)
    其中  imgviewobj：基本结构同上imgobj，其中增加imgviewobj.index (表示当前焦点图)
         
          

##### Demo
   参考  ynGalleryDemo 示例  放入HBX中运行
   
   
   
##### 注意
   请用HBX1.8以上版本（该版本起对于滑动操作提高了性能，特别是APP平台）




#### 结束  感谢！

