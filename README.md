关键技术与对应代码说明
 
1. HTML+CSS页面布局美化技术
- 技术点：弹性flex布局、网格grid布局、线性渐变、圆角、hover悬浮动效、移动端媒体自适应；
- 对应代码：页面全部 <div> 容器、 <style> 完整样式块；
- 作用：搭建搜索、今日天气、预报三大模块，美化界面，适配电脑与手机。
 
2. JS离线静态数据存储技术
- 技术点：JS对象字面量存储模拟气象数据；
- 对应代码： const fullRegionDB = {}  全局对象；
- 作用：预存全国省市区温度、天气、5天预报数据，无任何网络请求，彻底规避fetch、JSON解析报错。
 
3. 城市检索匹配逻辑
- 技术点：字符串去空校验、精准匹配、模糊关键词循环检索；
- 对应代码： searchRegion(inputText)  函数；
- 作用：校验输入非空，遍历地区库匹配数据，检索成功后调用渲染函数。
 
4. DOM动态渲染技术
- 技术点：元素获取 getElementById 、动态创建卡片 createElement 、文本填充 innerHTML ；
- 对应代码： renderWeather(cityNameText, data)  函数；
- 作用：动态更新页面标题（今日天气：XX）、实时温度、生成5天预报卡片，控制模块显隐。
 
5. localStorage本地持久化存储
- 技术点： localStorage.setItem 写入、 localStorage.getItem 读取缓存；
- 对应代码： window.onload 页面加载读取逻辑、搜索函数内缓存写入代码；
- 作用：保存上次搜索城市，页面刷新后自动恢复历史查询结果。
 
6. 浏览器Geolocation定位API
- 技术点：原生 navigator.geolocation.getCurrentPosition 获取设备坐标；
- 对应代码：定位按钮 locBtn 点击监听事件；
- 作用：获取用户位置，直接匹配佛山本地数据；区分不支持、拒绝权限、超时三类异常并弹窗提示，不调用第三方接口，无跨域报错。
 
7. 交互事件监听
- 技术点： addEventListener 绑定click点击、keydown键盘回车事件；
- 对应代码：搜索按钮、输入框、定位按钮的事件绑定代码；
- 作用：实现点击查询、回车快速检索、一键定位三种交互方式。
 
8. 容错防报错处理
- 技术点：前置空值判断、分支异常捕获；
- 对应代码：检索、定位、渲染函数内所有if判断提示逻辑；
- 作用：避免空输入、无匹配城市、定位失败导致页面渲染崩溃，本地file协议双击即可运行，无需Live Server。
