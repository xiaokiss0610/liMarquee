<h1>使用方法</h1>

1、引入文件

    <link rel="stylesheet" href="/css/liMarquee.css">
    <script src="/js/jquejquery-1.8.3.min></script>
    <script src="/jquery.liMarquee.js"></script>

2 ， html

    <h1>默认效果</h1>
    <ul class="demo">
        <li>默认效果是向左滚动</li>
        <li>不传递参数</li>
        <li>默认效果是向左滚动</li>
        <li>默认效果是向左滚动</li>
        <li>默认效果是向左滚动</li>
    </ul>

    <h1>向右滚动</h1>
    <div class="demo2">
        <a>向右滚动</a>
        <a>传递一个</a>
        <a>参数对象</a>
        <a>direction：right</a>
        <a>向右滚动</a>
    </div>
    <div class="left">
        <h1>向上滚动</h1>
        <div class="demo3">
            <ul>
                <li>向上滚动</li>
                <li>传递一个</li>
                <li>参数对象</li>
                <li>direction：up</li>
                <li>向上滚动</li>
            </ul>
        </div>

        <h1>向下滚动</h1>
        <div class="demo4">
            <ul>
                <li>向下滚动</li>
                <li>传递一个</li>
                <li>参数对象</li>
                <li>direction：down</li>
                <li>向下滚动</li>
            </ul>
        </div>
    </div>
    <div class="right">
        <h1>向上滚动 速度值20</h1>
        <div class="demo5">
            <ul>
                <li>向上滚动</li>
                <li>传递一个</li>
                <li>参数对象</li>
                <li>direction：up</li>
                <li>向上滚动</li>
            </ul>
        </div>

        <h1>向下滚动 速度值200</h1>
        <div class="demo6">
            <ul>
                <li>向下滚动</li>
                <li>传递一个</li>
                <li>参数对象</li>
                <li>direction：down</li>
                <li>向下滚动</li>
            </ul>
        </div>
    </div>

    <h1>图片演示</h1>
    <div class="demo7">
        <img src="images/1.jpg" alt="">
        <img src="images/1.jpg" alt="">
        <img src="images/1.jpg" alt="">
        <img src="images/1.jpg" alt="">
        <img src="images/1.jpg" alt="">
        <img src="images/1.jpg" alt="">
        <img src="images/1.jpg" alt="">
        <img src="images/1.jpg" alt="">
        <img src="images/1.jpg" alt="">
    </div>

3 , script

        $(function () {
            //不传参数是默认效果
            $('.demo').liMarquee();

            //传入一个对象参数 向右滚动
            $('.demo2').liMarquee({
                direction: 'right'
            });

            //传入一个对象参数 向上滚动
            $('.demo3').liMarquee({
                direction: 'up'
            });

            //传入一个对象参数 向下滚动
            $('.demo4').liMarquee({
                direction: 'down'
            });


            //传入一个对象参数 向上滚动+滚动速度
            $('.demo5').liMarquee({
                direction: 'up',
                //滚动速度 值越大滚动越快
                scrollamount: 20
            });

            //传入一个对象参数 向下滚动+滚动速度
            $('.demo6').liMarquee({
                direction: 'down',
                //滚动速度 值越大滚动越快
                scrollamount: 200
            });

            
            //传入一个对象参数 向下滚动+滚动速度
            $('.demo7').liMarquee();
        })
        

4 , 参数


        名称            类型        默认值          说明 
        
        direction	    字符串	    left	滚动方向，可选 left / right / up / down
        loop	        整数	        -1	    循环次数，-1 为无限循环
        scrolldelay	    整数    	    0   	    每次重复之前的延迟
        scrollamount	整数	        50	    滚动速度，越大越快
        circular	    布尔值	    true	无缝滚动，如果为 false，则和 marquee 效果一样
        drag	        布尔值	    true	鼠标可拖动
        runshort	    布尔值	    true	内容不足是否滚动
        hoverstop	    布尔值	    true	鼠标悬停暂停
        xml	            布尔值	    false	加载 xml 文件
        inverthover	    布尔值  	    false	反向，即默认不滚动，鼠标悬停滚动