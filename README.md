# rule
规则

根据gulp的文档，它努力实现的主要特性是：

易于使用：采用代码优于配置策略，gulp让简单的事情继续简单，复杂的任务变得可管理。
高效：通过利用node.js强大的流，不需要往磁盘写中间文件，可以更快地完成构建。
高质量：gulp严格的插件指导方针，确保插件简单并且按你期望的方式工作。
易于学习：通过把API降到最少，你能在很短的时间内学会gulp。构建工作就像你设想的一样：是一系列流管道。
Gulp通过流和代码优于配置策略来尽量简化任务编写的工作。
别的先不说，通过代码来比较两者（gulp VS grunt） 可以参照我的代码，也可以阅读该文章。

Gruntfile.js
gulpfile.js
两者的功能基本类似，gulp是通过代码完成任务，体现了代码优于配置的原则，对程序员更加友好，另外它也可以将多个功能一次性串起来，不需要暂存在本地，体现了对流的使用，这个可以阅读该文章里的例子。

另外，经常会有人问，为什么gulp比grunt快，这个可以参考这篇文章 或者我本人在segmentfault上得回答编译同样的scss，为什么gulp的速度几乎是grunt的两倍?

关于NodeJS流(stream)

因为gulp是基于流的方式工作的，所以想要进一步深入gulp，我们应该先学习NodeJS的流, 当然即使对流不熟悉，依然可以很方便的使用gulp。

资料
NodeSchool stream-adventure
stream-handbook
相关视频
How streams help to raise Node.js performance
Node.js streams for the utterly confused
常用资料

Gulp官网 http://gulpjs.com/
Gulp中文网 http://www.gulpjs.com.cn/
Gulp中文文档 https://github.com/lisposter/gulp-docs-zh-cn
Gulp插件网 http://gulpjs.com/plugins/
Awesome Gulp https://github.com/alferov/awesome-gulp
StuQ-Gulp实战和原理解析 http://i5ting.github.io/stuq-gulp/
glob用法 https://github.com/isaacs/node-glob
gulp常用插件

流控制

event-stream 事件流，不是插件但很有用
gulp-if 有条件的运行一个task
gulp-clone Clone files in memory in a gulp stream 非常有用
vinyl-source-stream Use conventional text streams at the start of your gulp or vinyl pipelines
AngularJS

gulp-ng-annotate 注明依赖 for angular
gulp-ng-html2js html2js for angular
gulp-angular-extender 为angular module添加dependencies
gulp-angular-templatecache 将html模板缓存到$templateCache中
文件操作

gulp-clean 删除文件和目录, 请用del来代替它Example
gulp-concat 合并文件
gulp-rename 重命名文件
gulp-order 对src中的文件按照指定顺序进行排序
gulp-filter 过滤文件 非常有用 Example
gulp-flatten 当拷贝文件时，不想拷贝目录时使用 segmentfault
压缩

gulp-minify-css压缩css
gulp-uglify 用uglify压缩js
gulp-imagemin 压缩图片
gulp-minify-html 压缩html
gulp-csso 优化CSS
工具

gulp-load-plugins 自动导入gulp plugin
gulp-load-utils 增强版gulp-utils
gulp-task-listing 快速显示gulp task列表
gulp-help 为task添加帮助描述
gulp-jsdoc 生成JS文档
gulp-plumber Prevent pipe breaking caused by errors from gulp plugins Example
yargs 处理 process.argv
run-sequence 顺序执行 gulp task，gulp 4.0 已经支持该功能 gulp.series(...tasks)
gulp-notify gulp plugin to send messages based on Vinyl Files
gulp-shell 非常有用
gulp-grunt 在gulp中运行grunt task
JS/CSS自动注入

gulp-usemin Replaces references to non-optimized scripts or stylesheets into a set of HTML files
gulp-inject 在HTML中自动添加style和script标签 Example
wiredep 将bower依赖自动写到index.html中 Example
gulp-useref 功能类似与usemin Example 新版本用法有变化，详见gulp-useref的README.md
代码同步

browser-sync 自动同步浏览器，结合gulp.watch方法一起使用 Example 1 Example 2
gulp-nodemon server端代码同步
Transpilation

gulp-babel 将ES6代码编译成ES5 Example
babelify Browserify transform for Babel
gulp-traceur Traceur is a JavaScript.next-to-JavaScript-of-today compiler
打包

gulp-browserify 用它和 babelify 实现ES6 module Example
编译

gulp-less 处理less Example
gulp-sass 处理sass
代码分析

gulp-jshint JSHint检查 Example
gulp-jscs 检查JS代码风格 Example
特别推荐

gulp-changed 只传输修改过的文件
gulp-cached 将文件先cache起来，先不进行操作
gulp-remember 和gulp-cached一块使用
gulp-newer pass through newer source files only, supports many:1 source:dest
其他

webpack-stream gulp与webpack Example
gulp-autoprefixer Prefix CSS
gulp-sourcemaps 生成source map文件
gulp-rev Static asset revisioning by appending content hash to filenames: unicorn.css → unicorn-d41d8cd98f.css
gulp-rev-replace Example
gulp-iconfont 制作iconfont Example
gulp-svg-symbols 制作SVG Symbols, 关于使用SVG Symbol
gulp-template 模板替换
gulp-dom-src 将html中的script，link等标签中的文件转成gulp stream。
gulp-cheerio Manipulate HTML and XML files with Cheerio in Gulp.
require-dir 利用它我们可以将 gulpfile.js 分成多个文件，具体用法可以参考这个Splitting a gulpfile into multiple files
gulp入门视频

Learning Gulp (youtube)

Learning Gulp #1 - Installing & Introducing Gulp
Learning Gulp #2 - Using Plugins & Minifying JavaScript
Learning Gulp #3 - Named Tasks
Learning Gulp #4 - Watching Files With Gulp
Learning Gulp #5 - Compiling Sass With Gulp
Learning Gulp #6 - Keep Gulp Running With Plumber
Learning Gulp #7 - Handling Errors Without Plumber
Learning Gulp #8 - LiveReload With Gulp
Learning Gulp #9 - Easy Image Compression
Learning Gulp #10 - Automatic Browser Prefixing
Learning Gulp #11 - Gulp Resources & What's Next
Get started with gulp(youtube)

Get started with gulp Part 1: Workflow overview and jade templates
Get started with gulp Part 2: gulp & Browserify
Get started with gulp Part 3: Uglify & environment variables
Get started with gulp Part 4: SASS & CSS minification
Get started with gulp Part 5: gulp.watch for true automation
Get started with gulp Part 6: LiveReload and web server
Gulp in Action (慕课网)

Gulp in Action(一)
Gulp in Action(二)
Gulp in Action(三)
BGTSD (youtube)

BGTSD - Part 20: Gulp and Babel Basics
BGTSD - Part 21: TypeScript and Gulp Basics
John Papa(付费)

JavaScript Build Automation With Gulp.js
gulp精彩文章

Using GulpJS to Generate Environment Configuration Modules
Introduction to Gulp.js
Merging multiple GulpJS streams into one output file
Getting ES6 modules working thanks to Browserify, Babel, and Gulp
Gulp学习指南系列：
Gulp学习指南之入门
Gulp学习指南之CSS合并、压缩与MD5命名及路径替换
6 Gulp Best Practices :star:
Automate all Imports (gulp-inject, wiredep, useref and angular-file-sort)
Understand directory structure requirements
Provide distinct development and production builds (browser-sync)
Inject files with gulp-inject and wiredep ( gulp-inject and wiredep )
Create production builds with gulp-useref (gulp-useref)
Separate Gulp tasks into multiple files require('require-dir')('./gulp')
Gulp 范儿 -- Gulp 高级技巧 :star:
Gulp 错误管理 :star:
探究Gulp的Stream :star:
Gulp安装及配合组件构建前端开发一体化
Gulp入门指南
Gulp入门指南 - nimojs
Gulp入门教程
Gulp开发教程（翻译）
Gulp：任务自动管理工具 - ruanyifeng
BrowserSync — 你值得拥有的前端同步测试工具
Essential Plugins for Gulp :star:
10 things to know about Gulp :star:
Writing a gulp plugin :star:
Gulp Plugin 开发 :star:
前端 | 重构 gulpfile.js
gulp使用经验谈
Splitting a gulpfile into multiple files :star:
Make your Gulp modular
gulp 传参数 实现定制化执行任务 使用 gulp.env
gulp和ES6

在gulp中使用ES6 :star:
Using ES6 with gulp
gulp和babelify

Example
debug gulp task

Debugging Gulp.js Tasks
Debug command line apps like Gulp
gulp项目结构应用实例

gulp模式
gf-skeleton-angularjs
generator-hottowel
generator-gulp-angular
generator-gulper
gulp常见问题 segmentfault之gulp

如何拷贝一个目录?
gulp.src([ files ], { "base" : "." })
