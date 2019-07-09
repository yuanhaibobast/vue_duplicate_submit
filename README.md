# vue_duplicate_submit
vue版本防止重复提交
# 代码思路
    ## 1 点击按钮，按钮disabled，等待1秒，如果一秒中没发请求，按钮恢复
    ## 2 一秒中之内有发请求，等待请求完成
    ## 3 完成后按钮恢复

# 代码说明
源代码在vue-duplication.html文件中，有示例和注释
# 指令--duplication
    button使用该指令后可实现防止重复提交
# 指令--duplicationHead
    使用场景
       点击删除按钮，弹出确认框，点击确认发送请求
    使用方法
       删除按钮使用duplicationHead指令，确认和取消按钮使用duplication按钮
# 插件的参数说明
    Vue.use(DduplicationPlugin, { interceptor: 'vueResource',buttonOpt:'component' });
    Vue.use(DduplicationPlugin, { interceptor: 'axios',buttonOpt:'elm' });
  ## interceptor
    默认实现vueResource和axios拦截器
    也可自定义拦截器，直接实现
  ## buttonOpt
    默认实现elm和component
    自定义实现需要实现disabled: function(button,vnode,value)和wait: function(button,vnode,value)方法
    具体可参考源代码码
 
 # 作者邮件，516194844@qq.com，前后端都行，求职中。。。。 
