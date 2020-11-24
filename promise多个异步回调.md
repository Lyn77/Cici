###promise解决多个异步回调问题
1. example
```
第一个service.toPromise().then(aa => {
  //处理第一个结果
  return 调用第二个方法。toPromise();
}).then(bb=> {
  //处理第二个结果
}).catch(cc=>{
  //处理异常
});
```
2. 变更检测机制
```
//数据绑定变更的时候用ChangeDetectorRef驱动angular更新视图
this.changeDetector.detectChanges();
```
