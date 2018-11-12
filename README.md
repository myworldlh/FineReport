# FineReport

```需要在网页中获取报表填报页面的一个按钮，并执行点击事件：
document.getElementById('reportFrame').contentWindow.contentPane.getWidgetByName('控件名').fireEvent('click') 
//////获取控件
contentPane.parameterEl.getWidgetByName('widgetname')
contentPane.getWidgetByName("TYPE_DIV");

取实际值 Widget.getValue() 获取控件实际值
取显示值 Widget.getText() 获取控件的显示值
赋实际值 Widget.setValue() 给参数控件赋值，不建议给填报控件赋实际值
赋显示值 Widget.setText() 给参数控件赋显示值
重置 Widget.reset() 清空数据
可见 Widget.visible() 设置控件可见
不可见 Widget.invisible() 设置控件不可见
是否可见 Widget.isVisible() 返回控件是否可见，返回true可见，false不可见
设置可见 Widget.setVisible(boolean) 设置控件是否可见，参数为true可见，false不可见
设置可用 Widget.setEnable(boolean) 设置控件是否可用，参数为true可用，false不可用
是否可用 Widget.isEnabled() 返回控件是否可用，返回true可用，false不可用
调用控件事件 Widget.fireEvent("事件名称") 设置控件触发指定名字的事件
是否可以为空 Widget.options.allowBlank=false 设置控件是否可为空，true可为空，false不可为空

contentPane常用属性
parameterEl 返回对象参数界面
curLGP 返回curLGP对象，只有填报预览及表单预览下才有
currentPageIndex 当前所在页，只有分页预览才有
reportTotalPage 总页数，只有分页预览报表才有
zoom 缩放比例

contentPane常用方法
方法 说明
appendReportRC(num) 在选中行后面插入num行，只有填报表才可以用
deleteReportRC() 删除指定行，只有填报表才可以用
deleteRows(param) 批量删除param所在记录，param为一窜单元格坐标的字符串数组
emailReport() 邮件发送
exportReportToExcel('指定格式') 参数为page时分页导出；simple原样导出；sheet分页分sheet导出
exportReportToImage() 输出图片
exportReportToPDF() 输出pdf
exportReportToWord() 输出word
fireEvent() 触发事件
appletPrint() applet打印
flashPrint() flash打印
getWidgetByName() 获取填报页面的控件
getCellValue(cell)/getCellValue(col,row) 获取单元格值，只有填报下有 
contentPane.curLGP.setCellValue(cell,null,str) 赋值
gotoFirstPage() 跳转到第一页，只有分页预览报表有
gotoLastPage() 跳转到最后一页，只有分页预览报表有
gotoPreviousPage() 跳转到上一页，只有分页预览报表有
gotoNextPage() 跳转到下一页，只有分页预览报表有
gotoPage(num) 跳转到指定num页，只有分页预览报表有
importExcelData() 在线导入excel，只有填报表才可以用
on() 监听
pdfPrint() pdf打印
printPreview() 打印预览，只有数据分析时才有
pageSetup() 页面设置，只有数据分析才有
scale(str) 缩放，str为"+"时放大，为"-"时缩小
setCellValue(cell,null,value)/setCellValue(col,row,value) 给单元格赋值，只有填报表才有
verifyReport() 数据校验，只有填报表才可以用
writeReport() 校验并提交报表，只有填报表才可以用
stash(undefined,ture) 暂存，第一个参数是按钮，第二个参数是是否提示成功，也可以不传参


contentPane监听事件
通过上述中的contentPane.on()来监听下述事件。
方法 说明
startload 加载起始
afterload 加载结束
```
