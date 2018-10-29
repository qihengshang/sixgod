# sixgod
## 我的负责模块：手动更新 ##
手动更新天气.概要设计 

     1. WeatherActivity中在onCreate()方法中获取到SwipeRefrshLayout的实例。 
     
     2. 调用setColorSchemeResources()方法来设置下拉刷新进度条的颜色，调用setOnRefreshListener()方法来设置一个下拉刷新的监听器。 
     
     3. 当触发了下拉刷新操作的时候，就会回调这个监听器的onRefresh()方法，再调用requestWeather()方法请求天气信息。 
     
     4. 当请求结束后，还需要调用SwipeRefrshLayout的setRefreshing()方法并传入false，表示刷新事件结束。

 
 
切换城市.概要设计 

     1.WeatherActivity中在onCreate()方法中获取到新增的DrawerLayout和Button的实例，然后在Button的点击事件中调用DrawerLayout的openDrawer()方法来打开滑动菜单。 
     
     2.在ChooseAreaFragment中根据状态的不同进行不同的看逻辑处理。如果在MainActivity当中，处理逻辑不变。 
     
     3.如果在WeatherActivity当中，关闭滑动菜单，显示下拉刷新进度条，请求获取新城市的天气信息。
