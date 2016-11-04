# angular_animate
angular animate

步骤一：通过设置
ng-leave
ng-leave-active 
ng-enter 
ng-enter-active（这些是ng内置的）来给ng应用添加动画

.page {
    position: absolute;
    width: 100%;
}
.page.ng-enter,
.page.ng-leave {
    -webkit-transition: .5s linear all;
    -moz-transition: .5s linear all;
    -ms-transition: .5s linear all;
    -o-transition: .5s linear all;
    transition: .5s linear all;
}
.page.ng-leave {
    left: 0;
    opacity: 1;
}
.page.ng-leave.ng-leave-active {
    left: -100%;
    opacity: 0;
}
.page.ng-enter {
    left: 100%;
    opacity: 0;
}
.page.ng-enter.ng-enter-active {
    left: 0;
    opacity: 1;
}


步骤二：引入angular-animate.js文件，并在模块的声明时，在依赖数组中加入ngAnimate

添加前：
var app = angular.module('kaifanla',['ng','ngRoute']);
添加后：
var app = angular.module('kaifanla',['ng','ngRoute','ngAnimate']);


步骤三：测试页面的跳转是否有动画效果


