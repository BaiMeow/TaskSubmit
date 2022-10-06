# 杭电二面后端任务日志及总结
## 写在前面
对于我一个什么都不会的菜鸟来说,这次任务繁重。但我还是想在繁忙之中抽出时间来写这篇日志,对的,日志,我真真想写的是一篇日志,总结只是要求写。关于我写日志的目的,主要是我想记录一下我这一段时间的成长,我学到了什么,所以我会以时间顺序来写,初步计划是每天都写,顺便记录一下生活,这可能会非常想日记,主要是给我自己看的,如果你们不感兴趣,可以直接跳到总结部分。总结会是我在任务完成后写。
## 日志
### 9月24日之前
在任务之前,先想想我会什么。但总体浏览了一下任务发现我真的什么都不会,要学的真的很多。	
* Go环境:没有搭建
* Go语言:零基础
* Http协议:没有接触过
* Gin框架:听都没听过
 
 好在我在一面上听取了学长写博客的建议,在这段时间内因为博客的需要,学会了Markdown的语法,所以才能自如地写这篇日志及总结了。这是我的博客地址<https://nothingalr8.top/.>博客刚搭建没多久,如今又在准备二面,没有什么内容,看了部分学长的博客后,我自愧不如,但我希望自己能坚持写下去。

### 9月24日(星期六)
今天是任务发放的第一天,看完任务介绍之后,我是惶恐的,感到了任务的繁重与紧迫,匆匆忙忙开始了学习。

今天的中心放在了Go环境的搭建和Go基础语法的学习上。根据我装Clion和Pycharm的经验,很快的安装好了GoLand,但是环境变量的设置让我稍微废了点功夫,但是很快就解决了。环境的搭建算是顺利完成了。而Go语法的学习,在刚开始还算轻松,跟着GoTour教程,一步步走下来直到切片,我卡住了。
```
package main
import "fmt"
func main() {
	s := make([]int, 0, 6)
	s = []int{2, 3, 5, 7, 11, 13}
	printSlice(s)

	// 截取切片使其长度为 0
	s = s[3:4]
	printSlice(s)

	// 拓展其长度
	s = s[:3]
	printSlice(s)

	// 舍弃前两个值
	s = s[2:]
	printSlice(s)
}
func printSlice(s []int) {
	fmt.Printf("len=%d cap=%d %v\n", len(s), cap(s), s)
}
```
我无法理解切片长度与容量的变化,以及s变为无元素的切片之后,对它再取切片,又出现了元素。
我并没有着急解决这个问题,结束了今天的学习。

### 9月25日(星期天)
今天一早看了[这篇文章](https://gw9u39xwqi.feishu.cn/wiki/wikcn1a3DQ1w3VcXkMYmLVztEoc)后,感谢良多。想从另一种角度来学习——直接从任务开始。
1. 根据教程,我安装了gin架构,但在goland中,我多次遇到了导入出错的问题,但不知怎么又解决了。
2. 我初步了解了http协议,知道了什么是GET,什么是POST,并在搜索引擎上搜索gin项目登入的教程,顺利做出了可以访问的页面。
3. 我逐步接触到了HTML,为了实现跳转按钮与登入,我学了botton标签,了解了表单。也完成了初步的跳转与登入(这是我甚至不知道什么是接口)但这与我设想的最终实现效果相差甚远,我也明白了最终任务并不会容易。
4. 最后,我重拾了很久之前用过的git(我已经不会用了),把项目push到了GitHub上。

### 9月26日(星期一)
今天很忙。一整天的课,没有什么时间来做任务,只是简单地看了一下go教程,没什么太大的收获。

### 9月27日(星期二)
今天依旧是非常忙的一天,也是一整天的课。但是今天晚上还是抽出了2个小时来继续任务,我觉得还算是有很多收获的。
1. 我安装了MySQL,配置好了环境,我希望在我的系统中加入数据库功能。
2. 我了解了一些项目文件的管理,将项目分成多个包,将特定文件放在特定文件夹中,我也决定将我的项目推倒重做,我也删除了GitHub上的库。
3. 我学习了gin的一些初步函数。
4. 我使用gorm链接起了数据库与go。

### 9月28日(星期三)
今天终于闲下来了,白天都没有课。而我的任务在今天也初步完成了,我感到非常有成就感。讲讲今天做了什么吧。
1. 重新规划好文件,理清了项目。
2. 重新完善了程序,实现了网页的运行。
3. 链接数据库,对登入注册进行了验证。
4. 使用内网穿透的方式,测试了项目在手机上的运行。

### 9月29日(星期四)
摆烂一整天。

### 9月30日(星期五)
准备开始部署服务器,遇到的麻烦数不胜数。在腾讯云的服务器上安装了Ubuntu,但是只有一个终端界面,没有任何图形化界面,对于我一个刚接触linux的新手极不友好。接下来分点来详细说明我遇到的困难。
1. 我被浏览器背刺了。当我好不容易学会用apt装软件的时候,安装过程每次都会莫名其妙的结束,网页报错(内存不足),再等我重新登入、重新安装时,linux报错了,我迫不得已重装了系统。而我始终没有意识到这是浏览器的原因。我检查了我电脑的内存,还剩8g;检查了服务器的内存。我就是没有想到是浏览器的原因,最后重装了系统十余次。直到下午无意中换了个浏览器,解决了这个问题。
2. 我又被腾讯云背刺了。我实在没有想到腾讯云不能直接使用图形化界面。在我好不容易安装好图形化界面后,发现不管怎么重启都没法进入图形化界面。后来看了腾讯云提供的文档之后,安装了vnc,也成功的运行了图形化界面,但是这个速度让我想起了自己家里的第一台电脑。最后,我放弃了图形化界面,开始学习命令行。
3. 

### 10月1日(星期六)
今天是国庆节,寝室里就只有我一个人了,继续部署网页,依旧困难,但至少没有昨天那么曲折了。

### 10月2日(星期六)
今天回家,摆烂!

### 10月3日(星期一)
今天在家,摆烂!

### 10月4日(星期二)
今天又是摆烂的一天,不知道为什么,在家里就会放松,感觉没有什么动力去学习。

### 10月5日(星期三)
今天给项目加了加密,用的是sha256,用go带的包比较轻松的解决了,但遇到了一个较为麻烦的问题,\[\]type与string类型之间的转换,最后顺利解决了。对于sha256,我在发现了有较为简单的方法去解决后,也没有去学。聪明~~傻傻~~的我还在怎么解密sha256来进行验证登入上纠结了半天。

## 总结一(9.28可以跳过)
这是项目的初步总结,写于9月28日,我想以后再进行不断完善。并~~更新这篇~~重新写一篇总结。

### 项目的组成
*	controller:项目使用到的自定义函数基本写在这里
*	dao(Data Access Object):项目与数据库相关的代码
*	model :自定义数据类型,目前只有一个结构体
*	router:有关路由的代码
* 	templates:用于存储网页的html文件
* 	main :主函数

这是我第一次自己开始做一个项目,对于文件的管理以后应该是必须的吧,这是我的第一次尝试。

### 收获
~~独自一个人去做任务的感觉是别样的~~ 在贴心的学长做的文档的指导下去做任务的感觉是别样的,虽说是一个人,但是有别人的引导,有别人帮你做的规划,这种学习状态还是我比较熟悉的。虽说没有人去强加监管,但还是会有一种动力。这么几天下来,我收获了许多。而最大的收获,我觉得是我已经开始适应大学的节奏了——自己给自己做好学习安排,没有别人管你,自己在生活、学习与娱乐之间找到一个平衡点。我也开始慢慢享受这种自由感了,我也开始喜欢上自学的感觉了。说实话,我觉得有些大学老师并不适合教学这一项工作,他们的课堂并不有趣生动,节奏也不适合我,这时候自学至关重要。不能因为不习惯一个老师,不习惯一个课而放弃一门学科,应当去自学。我觉得,大学给予的自由是为了让我更好的安排自我的学习,而我觉得,这几天的学习让我的自学能力又增强了。

再来讲讲面试吧。我已经看了NX学长在博客上的那篇关于当面试官的文章,挺幽默有趣,原来你们也知道啊。

> 常理来说,应当是把第一排的桌椅反过来,让新人坐,然后第二排坐面试官,面对面交流
> 听上去很正常,不是吗?
> 但是真实的情况,是一种很恐怖的场景:
> 你作为 2022 级零基础新生,领头进入教室,然后看见快半个教室的人,全部安安静静的,每个人面前一台笔记本电脑,都在等着你坐下来
> ~~寄!为什么这么多人~~
> 然后你坐下来,发现半个班的人都在面你,你还能淡定嘛?
> ~~(后来听说有女生真的受不住)~~
> 我只能对前面那两三批的人道个歉:这真的是我们的失误,毕竟我们也没想到会有这么多人来 ,~~而且鄙人也是第一次当面试官~~
(上文来自NX的博客,[『随笔』面试官竟是我自己 —— 2022 杭助秋招面试工作感想](https://www.nickxu.top/2022/09/18/%E3%80%8E%E9%9A%8F%E7%AC%94%E3%80%8F2022-%E6%9D%AD%E5%8A%A9%E6%8B%9B%E6%96%B0%E9%9D%A2%E8%AF%95%E6%84%9F%E6%83%B3/))

而这也正是我人生中经历的第一次面试的场景,那种感觉我想我是不会忘记的。但是我还是从面试中有收获的,比如开了自己的博客。其次,我终于踏出了我勇敢的第一步,在众人面前我也有勇气去讲话了。我觉得面试的机会还是十分宝贵的。
~~我有一个设想:明年社团招新可不可以把每一个社团都报过去,去白嫖他们的面试来获取面试经验。~~


### 任务进行中...
我觉得目前项目还是有许多不足之处的,希望各位学长能给与我一些建议。在这里,我想讲讲我想做的。
1. 我已经租了一个linux的服务器,我想要在服务器上运行我的程序。但是,我对Linux一点也不了解,还是有许多要学习:环境配置、linux命令、linux文件的管理等等。
2. 我希望美化网页的界面。
3. 我还没有完整的学习go语言的语法,接口、方法只是初步了解,没有弄懂,而映射以及其他一些较为复杂的东西,甚至还没了解。
4. 我对http协议的了解也甚少,也只是停留在GET与POST,计划尽快看完《图解http》。
5. 文档中提到的鉴权我还没搞懂,需要去研究。


## 总结二(10.6)
### 项目组成
以包的形式对项目进行了简单管理。分为controller、dao、model、router、templates这几个包、以及一个main文件。
*	controller:项目使用到的自定义函数基本写在这里
*	dao:项目与数据库相关的代码
*	model :自定义数据类型,只有一个结构体
*	router:有关路由的代码
* 	templates:用于存储网页的html文件
* 	main :主函数

### 项目完成情况
实现了注册、登录、注销功能,并链接了数据库,对密码进行了加密。并实现了网页的cookie,以及管理员登入,并做了简易的查询用户信息功能。最后,完成了服务器的环境的配置,部署了网页到服务器上。
#### 注册
在注册界面路由添加注册请求,实现对数据库中用户的添加,对密码进行sha256加密,并生成用户的cookie,也存储在数据库中(进行了加密)。
#### 登入
当用户发送登入请求时,从数据库中寻找用户名,并验证密码,进行反馈。若用户登入成功,会写入cookie,并跳转到个人信息页面。并在个人信息界面加了cookie验证。
#### 注销
在个人信息页面添加注销功能,点击后删除用户cookie,并回到主界面。
#### 管理员界面
当用户在登录界面输入管理员账户时,会自动检测,并跳转到管理员界面。目前在这里只有退出与搜索,点击搜索按钮后跳转到搜索界面,输入用户名,可以在数据库中查找到用户信息,并显示在页面上。

#### 网页部署
这次任务中,我相对艰难的完成了网页的部署。从租服务器、域名,再到学习并配置linux环境,再到部署代码,修bug,使用nginx代理,完成了网页在服务其上的部署。[点击访问](http://121.5.133.250)。浏览器必然提醒不安全,我的域名暂时还没有通过备案,没有办法访问,我也没有找到可以直接给ip地址部署的ssl,请见谅.

### 遇见的问题
任务期间,我遇到了相当多的问题,有的顺利解决了,有的还没有解决。但每一个问题都耗费了我相当多的时间去解决它。几个小时、一个下午、甚至几天。接下来,我简单列举一下我所遇到的问题,并提供我的解决方式。
#### Go语法相关
在go语法方面遇到的问题还算小


| 问题 |问题描述| 解决方法|
|:--------: | :-----------: |:--------: |
| \[\]byte转换为string类型出错|使用string函数转换时会乱码,无法储存进数据库|使用fmt.Sprint函数|
| \[\]byte转换为string类型出错|使用string函数转换时会乱码,无法储存进数据库|使用fmt.Sprint函数|


#### gin与gorm
| 问题 |问题描述| 解决方法|
|:--------: | :-----------: |:--------: |
| \[\]byte转换为string类型出错|使用string函数转换时会乱码,无法储存进数据库|使用fmt.Sprint函数|
| \[\]byte转换为string类型出错|使用string函数转换时会乱码,无法储存进数据库|使用fmt.Sprint函数|


#### 网页部署
网页部署过,是我这次任务遇到问题最多的环节,我几度想要放弃。
| 问题 |问题描述| 解决方法|
|:--------: | :-----------: |:--------: |
| \[\]byte转换为string类型出错|使用string函数转换时会乱码,无法储存进数据库|使用fmt.Sprint函数|
| \[\]byte转换为string类型出错|使用string函数转换时会乱码,无法储存进数据库|使用fmt.Sprint函数|

### 个人收获
这次任务收获还算多吧
