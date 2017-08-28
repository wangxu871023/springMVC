hello github!
新建动态网站  NEW WEB  DYNAMIC WEB PROJECT  NEXT
修改output folder  www/WEB-INF/classes  NEXT
修改content dictionary  www
在www下新建index.jsp   body 添加 hello spring mvc!

PROJECT CLEAN

项目右键 RUN AS ON SERVER

问题出现  弹框 tomcat7.0 start fail
控制台出现错误
java.lang.IllegalArgumentException: Document base D:\wsframe\workspace\.metadata\.plugins\org.eclipse.wst.server.core\tmp0\wtpwebapps\oa does not exist or is not a readable directory

解决办法：删除之前的SERVER  右键SERVERS 删除

配置springMVC环境
首先在www/WEB-INF 全部copy  然后 src  全部copy

右键项目refresh  PROJECT clean  项目右键 RUN AS ON SERVER

==================================页面控制器===============================
首先打开UserController  (用户页面控制器)  就是个普通类
特别的是类的上面带了两个注解@Controller (标注控制器) @RequestMapping (请求处理器的映射规则)

然后页面控制器有很多方法 都返回的是String   特别的是带了注释 @RequestMapping (请求处理器的映射规则)
这些方法主要是处理用户的需求
^(*￣(oo)￣)^  UserController类上面的@RequestMapping (请求处理器的映射规则) 是 @RequestMapping("user")，方法上面的@RequestMapping("list")   结果是tomcat启动后在浏览器输入http://localhost:8080/lyb2.0/user/list  就会进入UserController类下的list方法。


参数的传递
    请求参数获取方式
    通过名称传递  适用于参数在2个以内情况
    浏览器user/view?id=25
    public String view(int id) {

    }

    页面传递从Controller传递给JSP
        ModelMap map
        map.addAttribute("user", userService.getByID(id));

===========================================================================

===========================================================================
