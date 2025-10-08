## UI编辑器一些问题

导入文件顺序影响后续资源的依赖`DescIndex.SC2Layout`：

```XML
<?xml version="1.0" encoding="utf-8" standalone="yes"?>
<Desc>
    <Include path="UI/Layout/CustomInfoPaneQueue.SC2Layout"/>
    <Include path="UI/Layout/CustomInfoPanel.SC2Layout"/>
    <Include path="UI/Layout/MainFrame.SC2Layout"/>
</Desc>

```

最原子的组件应该首先被导入，之后的依赖才能够正确找到对应的模板或者框架。