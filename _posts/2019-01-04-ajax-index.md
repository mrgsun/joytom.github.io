---
layout: post
title:  "这是我的开始"
categories: Personal
tags:  Personal
author: mrgsev
---

## AJAX：
##### 一、 ajax是什么？
Ajax==异步的JavaScript和xml ，创建快速动态网页的技术，通过后台与服务器进行少量数据交换，Ajax可以实现网页异步更新，也就是再不重新加载网页对部分进行更新，传统i的网页不使用Ajax，想要更新内容必须重新加载页面。
##### 二 、ajax一般用在什么哪里？
  简单来说用来连接数库，但是连接数据库传输的信息量很少，用不着重新加载整页面。避免属性整个页面带来资源浪费。
##### 三 、为什么要使用ajax？
使用ajax可以减轻服务器的负担，按需取数，可以最大程度减少冗余请求和响应服务器造成的负担，无需更新页面，减少用户心理和实际的等待时间。带来更好的用户体验。可以把以前一些服务器负担的工作转嫁到客户端，利用客户端闲置的能力来处理，减轻服务器和速写的负担，节约空间和宽带租用成本。可以调用外部数据。基于标准化的并被广泛支持的技术，不需要下载插件或者小程序。进一步促进页面呈现和数据的分离。
##### 四 、使用ajax
jQuery是js（JavaScript）的类库，里边封装了大量的js底层代码。
jquery的操作ajax提供了两种方法。
1. **$ajax()**
```php
$.ajax({
    url: "url" ,
    type: "get/post",
    dataType: "json",
    data: {userid:1},
    success:function(){

    },
    error:function() {
    }
})
```
2. **$.get()\$.post()**
```php
$.get(
            "url",
            {userID:"123"},
            function(response) {
            }
        );
```
或者、
```php
$.post(
            "url",
            {userID:"123"},
            function(response) {
            }
        );
```
案例：
```php
$(function(){
    $.ajax({
        type:"GET",
        url:"test.json",
        data:{username:$("#username").val()，content :$("#content").val()},
        dataType: "json",
        success: function(data){
            $('#resText').empty();//清空resText里边所有的值
        }
    })
})
```
传值：
```php
$.ajax({
    url: '',
    type:'post',
    data:{did:did},
    success:function(data){
        setTimeout(function(){
            window.localtion.reload();//页面刷新
          }，1000)；
    }，
    error：function（data){
        alert('2222');
    }
})
```
