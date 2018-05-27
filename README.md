# p1
目标1：先完成一个通信模块

Go实战--实现简单的restful api(The way to go)
https://blog.csdn.net/wangshubo1989/article/details/71128972

golang自带的http.SeverMux路由实现简单,本质是一个map[string]Handler,是请求路径与该路径对应的处理函数的映射关系。实现简单功能也比较单一：

不支持正则路由， 这个是比较致命的
只支持路径匹配，不支持按照Method，header，host等信息匹配，所以也就没法实现RESTful架构
而gorilla/mux是一个强大的路由，小巧但是稳定高效，不仅可以支持正则路由还可以按照Method，header，host等信息匹配，可以从我们设定的路由表达式中提取出参数方便上层应用，而且完全兼容http.ServerMux

github地址： 
https://github.com/gorilla/mux
