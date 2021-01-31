<center id="title"><h1>Python - 日历calendar、日期datetime、时间time模块详解</h1></center><hr>

<font size="3"><b>博主精心制作了该系列彩色高亮的动态链接模块手册，预期该手册比阅读纸质书籍有更友好、更便捷、更让人舒适的使用体验。希望大家喜欢。</b></font >
<hr>

[>点击此跳转到目录](#content)

为了更好的效果，推荐在博客中阅读：
https://blog.csdn.net/qq_28550263/article/details/112858076

<h3><font id="calendar" color="#004080" >1.日历模块calendar</font></h3>

[>回目录](#content)
[<font id="classCalendar" color="#008000" size="4"><b>1.1 Calendar类</b></font>](#calendar)

>`class calendar.Calendar(firstweekday=0)`
<b>创建一个 Calendar 对象。 </b>
> - <font id="firstweekday">firstweekday</font> 是一个整数，用于指定一周的第一天。 
> - 0 是星期一（默认值），6 是星期天。

>[<font id="iterweekdays" color="#AE5EFF" size="3"><b>iterweekdays()</b></font>](#classCalendar)
<b>返回一个迭代器:</b>
> - 迭代器的内容为一星期的数字。
> - 迭代器的第一个值与 [firstweekday 属性](#firstweekday )的值一至。

>[<font id="itermonthdates" color="#AE5EFF" size="3"><b>itermonthdates(year, month)</b></font>](#classCalendar)
<b>返回一个迭代器:</b>
> - 迭代器的内容为 year 年 month 月(1-12)的日期。
> - 这个迭代器返回当月的所有日期 ( [datetime.date 对象]())，日期包含了本月头尾用于组成完整一周的日期。

>[<font id="itermonthdays" color="#AE5EFF" size="3"><b>itermonthdays(year, month)</b></font>](#classCalendar)
<b>返回一个迭代器:</b>
> - 迭代器的内容与 [itermonthdates()](#itermonthdates) 类似，为 year 年 month 月的日期，但不受 datetime.date 范围限制。
> - 返回的日期为当月每一天的日期对应的天数。对于不在当月的日期，显示为 0。

>[<font id="itermonthdays2(year,month)" color="#AE5EFF" size="3"><b>itermonthdays2(year, month)</b></font>](#classCalendar)
<b>返回一个迭代器:</b>
> - 迭代器的内容与 [itermonthdates() ](#itermonthdates)类似为 year 年 month 月的日期，但不受 datetime.date 范围的限制。
> - 迭代器中的元素为一个由日期和代表星期几的数字组成的的元组。

>[<font id="itermonthdays3" color="#AE5EFF" size="3"><b>itermonthdays3(year, month)</b></font>](#classCalendar)
<b>返回一个迭代器:</b>
> - 迭代器的内容与 [itermonthdates()](#itermonthdates) 类似为 year 年 month 月的日期，但不受 datetime.date 范围的限制。
> - 迭代器的元素为一个由年，月，日组成的元组。

>[<font id="itermonthdays4" color="#AE5EFF" size="3"><b>itermonthdays4(year, month)</b></font>](#classCalendar)
<b>返回一个迭代器:</b>
> - 迭代器的内容与 [itermonthdates()](#itermonthdates) 类似为 year 年 month 月的日期，但不受 [datetime.date](#) 范围的限制。
> - 迭代器的元素为一个由年，月，日和代表星期几的数字组成的元组。


>[<font id="monthdatescalendar" color="#AE5EFF" size="3"><b>monthdatescalendar(year, month)</b></font>](#classCalendar)
<b>返回一个表示指定年月的周列表。</b>
> - 周列表由七个 [datetime.date 对象]()组成。

>[<font id="monthdays2calendar" color="#AE5EFF" size="3"><b>monthdays2calendar(year, month)</b></font>](#classCalendar)
<b>返回一个表示指定年月的周列表。</b>
> - 周列表由七个代表日期的数字和代表周几的数字组成的二元元组。

>[<font id="monthdayscalendar" color="#AE5EFF" size="3"><b>monthdayscalendar(year, month)</b></font>](#classCalendar)
<b>返回一个表示指定年月的周列表。</b>
> - 周列表由七个代表日期的数字组成。

>[<font id="yeardatescalendar" color="#AE5EFF" size="3"><b>yeardatescalendar(year, width=3)</b></font>](#classCalendar)
<b>返回可以用来格式化的指定年月的数据。</b>
> - 返回的值是一个列表，列表是月份组成的行。
>  - 每一行包含了最多 width 个月(默认为3)。
>  - 每个月包含了4到6周，每周包含1--7天。
>  - 每一天使用 [datetime.date 对象]()。

>[<font id="" color="#AE5EFF" size="3"><b>yeardays2calendar(year, width=3)</b></font>](#classCalendar)
<b>返回可以用来模式化的指定年月的数据(与 yeardatescalendar() 类似)。</b>
> - 周列表的元素是由表示日期的数字和表示星期几的数字组成的元组。
> - 不在这个月的日子为0。

>[<font id="yeardayscalendar" color="#AE5EFF" size="3"><b>yeardayscalendar(year, width=3)</b></font>](#classCalendar)
<b>返回可以用来模式化的指定年月的数据(与 [yeardatescalendar()](#yeardatescalendar) 类似)。</b>
> - 周列表的元素是表示日期的数字。
>  - 不在这个月的日子为0。

[<font id="classTextCalendar" color="#008000" size="4"><b>1.2 TextCalendar类</b></font>](#calendar)



>`class calendar.TextCalendar(firstweekday=0)`
<b>用于生成纯文本日历。</b>

<font size="2"><b>TextCalendar 实例有以下方法：</b></font>

>[<font id="formatmonth" color="#AE5EFF" size="3"><b>formatmonth(theyear, themonth, w=0, l=0)</b></font>](#classTextCalendar)
<b>返回一个多行字符串来表示指定年月的日历。</b>
> - w 为日期的宽度，但始终保持日期居中。
> - l 指定了每星期占用的行数。
> - 以上这些还依赖于构造器或者 setfirstweekday() 方法指定的周的第一天是哪一天。

>[<font id="prmonth" color="#AE5EFF" size="3"><b>prmonth(theyear, themonth, w=0, l=0)</b></font>](#classTextCalendar)
<b>与 [formatmonth() 方法](#formatmonth)一样，返回一个月的日历。</b>

>[<font id="formatyear" color="#AE5EFF" size="3"><b>formatyear(theyear, w=2, l=1, c=6, m=3)</b></font>](#classTextCalendar)
<b>返回一个多行字符串，这个字符串为一个 m 列日历。</b>
> - 可选参数 w, l, 和 c 分别表示日期列数， 周的行数， 和月之间的间隔。
> - 同样，以上这些还依赖于构造器或者 setfirstweekday() 指定哪一天为一周的第一天。
> - 日历的第一年由平台依赖于使用的平台。

>[<font id="pryear" color="#AE5EFF" size="3"><b>pryear(theyear, w=2, l=1, c=6, m=3)</b></font>](#classTextCalendar)
<b>与 [formatyear() 方法](#formatyear)一样，返回一整年的日历。</b>


[<font id="classHTMLCalendar" color="#008000" size="4"><b>1.3 HTMLCalendar类</b></font>](#calendar)

>`class calendar.HTMLCalendar(firstweekday=0)`
<b>可以使用这个类生成 HTML 日历。</b>

<font size="2"><b>HTMLCalendar 实例有以下方法：</b></font>

>[<font  id="formatmonth" color="#AE5EFF" size="3"><b>formatmonth(theyear, themonth, withyear=True)</b></font>](#classHTMLCalendar)
<font color="#3F6943"><b>返回一个 HTML 表格作为指定年月的日历。 </font>
> - withyear 为真，则年份将会包含在表头，否则只显示月份。

>[<font  id="formatyear" color="#AE5EFF" size="3"><b>formatyear(theyear, width=3)</b></font>](#classHTMLCalendar)
<font color="#3F6943"><b>返回一个 HTML 表格作为指定年份的日历。 </font>
> - width (默认为3) 用于规定每一行显示月份的数量。

>[<font  id="formatyearpage" color="#AE5EFF" size="3"><b>formatyearpage(theyear, width=3, css='calendar.css', encoding=None)</b></font>](#classHTMLCalendar)
<font color="#3F6943"><B>返回一个完整的 HTML 页面作为指定年份的日历。</B></font> 
> - width*(默认为3) 用于规定每一行显示的月份数量。 
> - *css 为层叠样式表的名字。如果不使用任何层叠样式表，可以使用 None 。 encoding 为输出页面的编码 (默认为系统的默认编码)。

<font size="2"><b>HTMLCalendar 有以下属性，你可以重载它们来自定义应用日历的样式。</b></font>

>[<font id="cssclasses" color="#AE5EFF" size="3"><b>cssclasses</b></font>](#classHTMLCalendar)
<font color="#3F6943"><b>一个对应星期一到星期天的 CSS class 列表。</font>
> - 默认列表为cssclasses = ["mon", "tue", "wed", "thu", "fri", "sat", "sun"]
> - 可以向每天加入其它样式cssclasses = ["mon text-bold", "tue", "wed", "thu", "fri", "sat", "sun red"]
> - 需要注意的是，列表的长度必须为7。

>[<font id="cssclass_noday" color="#AE5EFF" size="3"><b>cssclass_noday</b></font>](#classHTMLCalendar)
<b>工作日的 CSS 类在上个月或下个月发生。
> - 3.7 新版功能.

>[<font id="cssclasses_weekday_head" color="#AE5EFF" size="3"><b>cssclasses_weekday_head</b></font>](#classHTMLCalendar)
<font color="#3F6943"><b>用于标题行中的工作日名称的 CSS 类 列表。默认值与 cssclasses 相同。
> - 3.7 新版功能.

>[<font id="cssclass_month_head" color="#AE5EFF" size="3"><b>cssclass_month_head</b></font>](#classHTMLCalendar)
<b>月份的头 CSS 类（由 formatmonthname() 使用）。默认值为 "month" 。
> - 3.7 新版功能.

>[<font id="cssclass_month" color="#AE5EFF" size="3"><b>cssclass_month</b></font>](#classHTMLCalendar)
<font color="#3F6943"><b>某个月的月历的 CSS 类（由 formatmonth() 使用）。默认值为 "month" 。
> - 3.7 新版功能.

>[<font id="cssclass_year" color="#AE5EFF" size="3"><b>cssclass_year</b></font>](#classHTMLCalendar)
<font color="#3F6943"><b>某年的年历的 CSS 类（由 formatyear() 使用）。默认值为 "year" 。
> - 3.7 新版功能.

>[<font id="cssclass_year_head" color="#AE5EFF" size="3"><b>cssclass_year_head</b></font>](#classHTMLCalendar)
<font color="#3F6943"><b>年历的表头 CSS 类（由 formatyear() 使用）。默认值为 "year" 。
> - 3.7 新版功能.
> - 需要注意的是，尽管上面命名的样式类都是单独出现的(如： cssclass_month cssclass_noday), 但我们可以使用空格将样式类列表中的多个元素分隔开，例如：
>```python
>"text-bold text-red"
>```
>
>下面是一个如何自定义 HTMLCalendar 的示例
>```python
>class CustomHTMLCal(calendar.HTMLCalendar):
>    cssclasses = [style + " text-nowrap" for style in
>                  calendar.HTMLCalendar.cssclasses]
>    cssclass_month_head = "text-center month-head"
>    cssclass_month = "text-center month"
>    cssclass_year = "text-italic lead"
>```

[<font id="classLocaleTextCalendar" color="#008000" size="4"><b>1.4 LocaleTextCalendar类</b></font>](#calendar)

>`class calendar.LocaleTextCalendar(firstweekday=0, locale=None)`
> - 这个子类 TextCalendar 可以在构造函数中传递一个语言环境名称，并且返回月份和星期几的名称在特定语言环境中。
> - 如果此语言环境包含编码，则包含月份和工作日名称的所有字符串将作为 unicode 返回。

[<font id="classLocaleHTMLCalendar" color="#008000" size="4"><b>1.5 LocaleHTMLCalendar类</b></font>](#calendar)

>`class calendar.LocaleHTMLCalendar(firstweekday=0, locale=None)`
> - HTMLCalendar的这个子类可以在构造函数中被传递一个区域名称，并将返回指定区域中的月份和工作日名称。
> - 如果此区域设置包含编码，则包含月份和工作日名称的所有字符串都将作为unicode返回。
> -  这两个类的 formatweekday() 和 formatmonthname() 方法临时更改dang当前区域至给定 locale 。由于当前的区域设置是进程范围的设置，因此它们不是线程安全的。

[<font id="calendar_methods" color="#008000" size="4"><b>1.6 calendar模块中的其它方法和属性</b></font>](#calendar)
<font size="2"><b>[calendar 模块](#calendar)中的简单的文本日历方法：</b></font>

>[<font id="calendar.setfirstweekday(weekday)" color="#AE5EFF" size="3"><b>calendar.setfirstweekday(weekday)</b></font>](#calendar_methods)
<B>设置每一周的开始(0 表示星期一，6 表示星期天)。</B>
> - calendar还提供了 `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY` 和 `SUNDAY` 几个常量方便使用。
> - 例如，设置每周的第一天为星期天：
>```python
>import calendar
>calendar.setfirstweekday(calendar.SUNDAY)
>```

>[<font  id="calendar.firstweekday()" color="#AE5EFF" size="3"><b>calendar.firstweekday()</b></font>](#calendar_methods)
<font color="#3F6943"><b>返回当前设置的每星期的第一天的数值。</b></font>

>[<font id="calendar.isleap(year)" color="#AE5EFF" size="3"><b>calendar.isleap(year)</b></font>](#calendar_methods)
<font color="#3F6943"><b>如果 year 是闰年则返回 True ,否则返回 False。</b></font>

>[<font id="calendar.leapdays(y1,y2)" color="#AE5EFF" size="3"><b>calendar.leapdays(y1, y2)</b></font>](#calendar_methods)
<font  color="#3F6943"><b>返回在范围 y1 至 y2 （包含 y1 和 y2 ）之间的闰年的年数，其中 y1 和 y2 是年份。</b></font>
> - 此函数适用于跨越一个世纪变化的范围。

>[<font  id="calendar.weekday(year,month,day)" color="#AE5EFF" size="3"><b>calendar.weekday(year, month, day)</b></font>](#calendar_methods)
<font color="#3F6943"><b>返回某年（ 1970 -- ...），某月（ 1 -- 12 ），某日（ 1 -- 31 ）是星期几（ 0 是星期一）。</b></font>

>[<font  id="calendar.weekheader(n)" color="#AE5EFF" size="3"><b>calendar.weekheader(n)</b></font>](#calendar_methods)
<font color="#3F6943"><b>返回一个包含星期几的缩写名的头。</b> </font>
> - n 指定星期几缩写的字符宽度。

><font  id="calendar.monthrange(year,month)" color="#AE5EFF" size="3"><b>calendar.monthrange(year, month)</b></font>
<font color="#3F6943"><b>返回指定 年份 的指定 月份 的第一天是星期几和这个月的天数。</b></font>

>[<font  id="calendar.monthcalendar(year,month)" color="#AE5EFF" size="3"><b>calendar.monthcalendar(year, month)</b></font>](#calendar_methods)
<font color="#3F6943"><b>返回表示一个月的日历的矩阵。</b> </font>
> - 每一行代表一周；此月份外的日子由零表示。 
>  - 每周从周一开始，除非使用 setfirstweekday() 改变设置。

>[<font  id="calendar.prmonth(theyear,themonth,w=0,l=0)" color="#AE5EFF" size="3"><b>calendar.prmonth(theyear, themonth, w=0, l=0)</b></font>](#calendar_methods)
<font color="#3F6943"><b>打印由 month() 返回的一个月的日历。</b></font>

>[<font  id="calendar.month(theyear,themonth,w=0,l=0)" color="#AE5EFF" size="3"><b>calendar.month(theyear, themonth, w=0, l=0)</b></font>](#calendar_methods)
<font color="#3F6943"><b>使用 TextCalendar 类的 formatmonth() 以多行字符串形式返回月份日历。</font>

>[<font  id="calendar.prcal(year,w=0,l=0,c=6,m=3)" color="#AE5EFF" size="3"><b>calendar.prcal(year, w=0, l=0, c=6, m=3)</b></font>](#calendar_methods)
<font color="#3F6943"><b>打印由 calendar() 返回的整年的日历。</font>

>[<font  id="calendar.calendar(year,w=2,l=1,c=6,m=3)" color="#AE5EFF" size="3"><b>calendar.calendar(year, w=2, l=1, c=6, m=3)</b></font>](#calendar_methods)
<font color="#3F6943"><b>使用 TextCalendar 类的 formatyear() 返回整年的3列的日历以多行字符串的形式。</font>

>[<font  id="calendar.timegm(tuple)" color="#AE5EFF" size="3"><b>calendar.timegm(tuple)</b></font>](#calendar_methods)
<font color="#3F6943"><b>一个不相关但很好用的函数，它接受一个时间元组例如 time 模块中的 gmtime() 函数的返回并返回相应的 Unix 时间戳值，假定 1970 年开始计数， POSIX 编码。</b></font>
> - 实际上， time.gmtime() 和 timegm() 是彼此相反的。

<font size="2"><b>[calendar 模块](#calendar)包含以下数据属性：</b></font>

>[<font  id="calendar.day_name" color="#AE5EFF" size="3"><b>calendar.day_name</b></font>](#calendar_methods)
<font color="#3F6943"><b>在当前语言环境下表示星期几的数组。</b></font>

>[<font  id="calendar.day_abbr" color="#AE5EFF" size="3"><b>calendar.day_abbr</b></font>](#calendar_methods)
<font color="#3F6943"><b>在当前语言环境下表示星期几缩写的数组。</b></font>

>[<font  id="calendar.month_name" color="#AE5EFF" size="3"><b>calendar.month_name</b></font>](#calendar_methods)
<font color="#3F6943"><b>在当前语言环境下表示一年中月份的数组。</b></font>
> - 这遵循一月的月号为 1 的通常惯例，所以它的长度为 13 且 month_name[0] 是空字符串。

>[<font  id="calendar.month_abbr" color="#AE5EFF" size="3"><b>calendar.month_abbr</b></font>](#calendar_methods)
<font color="#3F6943"><b>在当前语言环境下表示月份简写的数组。</b></font>
> - 这遵循一月的月号为 1 的通常惯例，所以它的长度为 13 且 month_abbr[0] 是空字符串。

<h3><font id="datetime" color="#004080" >2.日期模块datetime</font></h3>

[>回目录](#content)
 - 待更新


<h3><font id="time" color="#004080" >3.时间模块time</font></h3>

[>回目录](#content)
 - 待更新

<br>
<br>
<hr>
附：
<hr>
<center><font id="content" size="5"><b> - 内 容 索 引 - </b></font></center>
<center>（点击超链接定向到相应位置）</center>

[>点击返回顶部](#title)

1 [日历模块calendar](#calendar)
1.1 [Calendar类](#classCalendar)
 | 项目 | 类型 | 说明 |
 |-|-|-|
 | [iterweekdays()](#iterweekdays) | 方法 | 返回迭代器，内容为一周的数字
 | [itermonthdates(year, month)](#itermonthdates) | 方法 | 返回迭代器，内容为 year 年 month 月(1-12)的日期
 | [itermonthdays(year, month)](#itermonthdays) | 方法 | 与itermonthdays()类似
 | [itermonthdays2(year, month)](#itermonthdays2(year,month)) | 方法 | 与itermonthdays()类似
 | [itermonthdays3(year, month)](#itermonthdays3) | 方法 | 与itermonthdays()类似
 | [itermonthdays4(year, month)](#itermonthdays4) | 方法 | 与itermonthdays()类似
 | [monthdatescalendar(year, month)](#monthdatescalendar) | 方法 | 返回一个表示指定年月的周列表
 | [monthdays2calendar(year, month)](#monthdays2calendar) | 方法 | 返回一个表示指定年月的周列表
 | [yeardayscalendar(year, width=3)](#yeardayscalendar) | 方法 | 与 yeardatescalendar() 类似

1.2 [TextCalendar类](#classTextCalendar)
 | 项目 | 类型 | 说明 |
 |-|-|-|
 | [formatmonth(theyear, themonth, w=0, l=0)](#formatmonth) | 方法 | 返回指定年月的日历 | 
 | [prmonth(theyear, themonth, w=0, l=0)](#prmonth) | 方法 | 返回一个月的日历 | 
 | [formatyear(theyear, w=2, l=1, c=6, m=3)](#formatyear) | 方法 | 返回一个多行字符串，这个字符串为一个 m 列日历 | 
 | [pryear(theyear, w=2, l=1, c=6, m=3)](#pryear) | 方法 | 返回一整年的日历 | 

1.3 [HTMLCalendar类](#classHTMLCalendar)

 | 项目 | 类型 | 说明 |
 |-|-|-|
 | [formatmonth(theyear, themonth, withyear=True)](#formatmonth) | 方法 | 返回一个多行字符串来表示指定年月的日历
 | [formatyear(theyear, width=3)](#formatyear) | 方法 | 返回一个多行字符串，这个字符串为一个 m 列日历
 | [formatyearpage(theyear, width=3, css=‘calendar.css’, encoding=None)](#formatyearpage) | 方法 | 返回一个完整的 HTML 页面作为指定年份的日历
 | [cssclasses](#cssclasses) | 属性 | 一个对应星期一到星期天的 CSS class 列表
 | [cssclass_noday](#cssclass_noday) | 属性 | 工作日的 CSS 类在上个月或下个月发生
 | [cssclasses_weekday_head](#cssclasses_weekday_head) | 属性 | 用于标题行中的工作日名称的 CSS 类 列表
 | [cssclass_month_head](#cssclass_month_head) | 属性 | 月份的头 CSS 类
 | [cssclass_month](#cssclass_month) | 属性 | 某个月的月历的 CSS 类
 | [cssclass_year](#cssclass_year) | 属性 | 某年的年历的 CSS 类
 | [cssclass_year_head](#cssclass_year_head) | 属性 | 年历的表头 CSS 类

1.4 [LocaleTextCalendar类](#classLocaleTextCalendar)

1.5 [LocaleHTMLCalendar类](#classLocaleHTMLCalendar)

1.6 [calendar模块函数和属性](#calendar_methods)
 | 项目 | 类型 | 说明 |
 |-|-|-|
 | [calendar.setfirstweekday(weekday)](#calendar.setfirstweekday(weekday)) | 函数 | 设置每一周的开始。
 | [calendar.firstweekday()](#calendar.firstweekday()) | 函数 | 返回当前设置的每星期的第一天的数值。
 | [calendar.isleap(year)](#calendar.isleap(year)) | 函数 | 判断是否是闰年。
 | [calendar.leapdays(y1, y2)](#calendar.leapdays(y1,y2)) | 函数 | 返回某两年间闰年的年数。
 | [calendar.weekday(year, month, day)](#calendar.weekday(year,month,day)) | 函数 | 返回某个日期是星期几。
 | [calendar.weekheader(n)](#calendar.weekheader(n)) | 函数 | 返回一个包含星期几的缩写名的头。
 | [calendar.monthrange(year, month)](#calendar.monthrange(year,month)) | 函数 | 返回指定月份的第一天是星期几与该月的天数。
 | [calendar.monthcalendar(year, month)](#calendar.monthcalendar(year,month)) | 函数 | 返回表示一个月的日历的矩阵。
 | [calendar.prmonth(theyear, themonth, w=0, l=0)](#calendar.prmonth(theyear,themonth,w=0,l=0)) | 函数 | 打印由 month() 返回的一个月的日历。
 | [calendar.month(theyear, themonth, w=0, l=0)](#calendar.month(theyear,themonth,w=0,l=0)) | 函数 | 以多行字符串形式返回月份日历。
 | [calendar.prcal(year, w=0, l=0, c=6, m=3)](#calendar.prcal(year,w=0,l=0,c=6,m=3)) | 函数 | 打印由 calendar() 返回的整年的日历。
 | [calendar.calendar(year, w=2, l=1, c=6, m=3)](#calendar.calendar(year,w=2,l=1,c=6,m=3)) | 函数 | 返回整年的3列的日历以多行字符串的形式
 | [calendar.timegm(tuple)](#calendar.timegm(tuple)) | 函数 | 接受一个时间元组例如 time 模块中的 gmtime() 函数的返回并返回相应的 Unix 时间戳值


2 [日期模块datetime](#datetime)

3 [时间模块time](#time)

<hr>
