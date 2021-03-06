# JKRefreshControl
仿<即刻>应用的下拉刷新方式

具体实现流程见Blog：[仿<即刻>下拉刷新效果实现](https://enjoysr.github.io/2016/10/09/%E4%BB%BF-%E5%8D%B3%E5%88%BB-%E4%B8%8B%E6%8B%89%E5%88%B7%E6%96%B0%E6%95%88%E6%9E%9C%E5%AE%9E%E7%8E%B0/)

开发环境：Xcode 8.0 (Swift 3.0)

## 效果图
![](https://raw.githubusercontent.com/EnjoySR/JKRefreshControl/master/ScreenShot/ScreenShot1.gif)

## 使用方式
与系统的 `UIRefreshControl` 一样，支持 UIScrollView 及其子类

- 添加控件

```swift
let refresh = JKRefreshControl()
tableView.addSubview(refresh)
```
- 添加刷新事件监听

```swift
refresh.addTarget(self, action: #selector(loadData), for: .valueChanged)
```

- 结束刷新

```swift
refresh.endRefreshing()
```

- 主动进入刷新状态

```swift
refresh.beginRefreshing()
```

## 其他
在控件进入到刷新状态，回到顶部的时候，刷新控件可能会有抖动，原因以及解决方法：[你的下拉刷新是否“抖”了一下](http://www.cnblogs.com/max5945/p/4283225.html)(在 iPhone 7 模拟器上有时候不好使，但是在真机上没有问题)

## License
MIT


