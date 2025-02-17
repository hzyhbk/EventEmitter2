# eventemitter2-cjs

修改源码，只导出 cjs 格式。

因为系统中如果额外使用了 systemjs 来加载 umd 模块，systemjs 会往 window 上挂 define 方法，eventemitter2@6.4.9 版本源码会先判断存在 define 方法就执行 amd 导出方式，就导致项目中使用 `import e from 'eventemitter2'` 拿到一个空对象。