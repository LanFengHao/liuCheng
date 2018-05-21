# 基本规范  

1.每个文件只包含一个React组件 （联系紧密的组件可以使用{命名空的形式}）；  
2.始终使用JSX语法，不要使用 React.creatElement 创建 ReactElement, 以提高编写速度、可读性、可维护性（没有 JSX 转换的特殊场景例外，如在 console 中测试组件）；  
3.使用 ES6 .  

## 命名规范

* 扩展名：使用 .js 作为 React 组件的扩展名；  
* 文件名： 使用大驼峰命名法， 如 MyComponent.js ；
* 组件命名：组件名称和文件名一致，使用大驼峰命名法,如MyComponent.js里的组件名应该是MyComponent；一个目录的根组件使用index.js命名，以目录名称作为组件名称；  
* 引用命名：React 组件使用大驼峰命名法， HTML标签、组件使用小驼峰命名法  
* 带命名空间的组件  
如果一个组件有许多关联子组件，可以以该组件作为命名空间编写、调用子组件。 
```
    var MyFormComponent = React.createClass({...});  
    MyFormComponent.Row = React.createClass({...}); 
    MyFormComponent.Label = React.createClass({...});
    MyFormComponent.Input = React.createClass({...});
    var Form = MyFormComponent;
    var App = ();
```

##### 不要使用 displayName 来命名组件，通过引用来命名。

### 引用来命名的写法
```
const ReservationCard = React.creatClass({

}）；

export defalut ReservationCard;
```
### 属性
##### 属性命名
* React组件的属性使用小驼峰命名法
* 使用 className 代替class属性
* 使用 htmlFor 代替for属性
* 传递给 HTML 的属性
* 传递给 HTML 元素的自定义属性,需要添加 data- 前缀,React 不会渲染非标准属性；
