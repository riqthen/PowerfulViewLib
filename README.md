[TOC]


[https://github.com/chaychan/PowerfulViewLibrary.git](https://github.com/chaychan/PowerfulViewLibrary.git)

1. 依赖ViewLib包           
2. 在布局文件中添加组件


# 添加组件
---
## 组件一 PowerfulEditText
**作用:**       
*可以给EditText自动添加删除全部文本,设置密码显示与否,在输入框两端设置图片,且可以控制图片大小,给右边按钮设置点击事件*

- **删除全部文本按钮**              
添加组件<com.riq.viewlib.PowerfulEditText />
在其中设置funcType属性      
`app:funcType="canClear"`   表示添加了清除文本按钮          

- **密码可见与否按钮**                          
`app:funcType="canWatchPwd"`    表示添加了密码可见与否按钮              
此处需要加上一个`android:inputType="textPassword"`,因为第一次进的时候是明文,但是按钮显示是输密码状态

- **在输入框两端设置图片**              
 添加如下属性即可
```
android:drawableLeft="@mipmap/ic_launcher"
android:drawableRight="@mipmap/ic_launcher"
app:leftDrawableHeight="40dp"
app:leftDrawableWidth="40dp"
app:rightDrawableHeight="30dp"
app:rightDrawableWidth="30dp" 
```

- **给输入框右边图片添加点击事件**
*可以用来添加搜索功能等*             
```
android:drawableRight="@mipmap/search"
```
执行点击事件方法 `powerfulEditText.setOnRightClickListener()`


---
## 组件二 手机号码格式化 PhoneEditText
**手机号码格式化输入,把手机号变为 'xxx xxxx xxxx'格式**
默认限定为只能输入11个数字              
*需要添加的属性*                
```
android:digits="0123456789 "    注意此处有"空格",因为格式化就是添加了一个空格
app:funcType="canClear"     //因为继承自PowerfulEditText,所以可以设置funcType属性
```
在java文件中,直接给pet.getTextString(),即可获取手机号码(去了空格)           


---
## 组件三 银行卡号码格式化BankCardNumEditText
**把银行卡号变为 'xxxx xxxx xxxx xxxx xxxx '格式**              
*需要添加的属性*                
```
android:maxEms="20"     此处未限制输入的长度, 所以此处可以限定长度
app:funcType="canClear"
android:digits="0123456789 "
```



