### jQuery.mPopup

这是一个多层级弹出窗口插件（Multilayer popup plugin => mPopup）,可以使用在项目中需要弹出多层窗口的情形。

基本使用方法：
```javascript
$.mPopup('Hello word!!!');
```

结合HTML
```html
    <body>
        <a id="open1" href="javascript:void(0);">Click here to pop up Box 1</a><br />
        <a class="open2" href="javascript:void(0);">Click here to pop up Box 2</a>
        <div class="box hidden" id="box1">
            <p>
                I am box 1.
            </p>
            <a class="open2" href="javascript:void(0);">Click me to open box 2!</a>
        </div>
        <div class="box none" id="box2">
            <p>
                Hi, I am box 2.<br />
                If you open me from Box 1, I will in front of box 1.
            </p>
            <a class="close" href="javascript:void(0);">Click here to close me</a>
       </div>
    </body>
    <script type="text/javascript">
        $(document).ready(function(){
            var box1 = $('#box1');
            $('#open1').click(function(){
                $.mPopup(box1,{
                    padding: 0         
                });
            });

            $('.open2').click(function(){
                $.mPopup($('#box2'),{
                    padding: 0,        
                    closeClass: ['close']
                });
            });
        });
    </script>
```


示例代码请下载：[完整mPopup项目](https://github.com/alvinhui/jquery.mPopup/archive/master.zip)
