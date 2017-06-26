### If you wan't learn anguar2 or 4 well,you must know more about the followings
### Router
- navigate(['/home',2]) 可以实现导航
### CanActivate
### CanDeactivate
### Resolve
### Observable(只要是Observable对象都可以使用map，filter方法，debounceTime需引入'rxjs/Rx')
流可以创建
- from
- of 
- range
- fromEvent(selector,event) map的时候必须指明事件的类型，可打印出来，再继续操作

```
import {Observable} from 'rxjs'
import 'rxjs/Rx'  ->使用debounceTime()
```
只要是Observable都可以订阅，那么哪些方法返回是Observable呢
1. 表单FormControl的valueChanges事件
2. http请求

### EventEmitter
实例拥有emit()方法，需点击事件触发
### ActivatedRouteSnapshot
router.snapshot:ActivatedRouteSnapshot
### ActivatedRoute 获取路由参数
- params['id']

### Http 使用时一定要用map方法以json方式返回
https://angular.cn/docs/ts/latest/api/http/index/Http-class.html 返回的都是Observable
```
this.http.get('person.json').map(res=>res.json())
```
### FormControl 
每一个input元素都是一个formControl，每一个formControl都有一个valueChanges事件
### @Input（）
### @Output（）
### @HostListener() 定义原生事件,也可以改名
```
@HostListener('mouseenter') onMouseEnter() {
    this.highlight('yellow');
  }
```
### Injectable() 自定义ts如guard需手动引入方可注入其他模块
### providers数组,里面放服务和guard，依赖注入的核心，找到后自动实例化
### imports[] 引入模块
如使用响应式form表单，就必须引入ReactiveFormsModule 否则就会报错
```

  imports: [
    BrowserModule,
    AppRoutingModule,
    HttpModule
  ],
```

### declarations数组 注册组件，模板即可使用eg:app-home
```
 declarations: [
    AppComponent,
    TestComponent,
    RangeComponent,
    FromComponent,
    EventComponent,
    EmitComponent,
    PromiseComponent,
    Promise1Component,
    AbmComponent
  ],
```