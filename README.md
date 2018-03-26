# ajax
##ajax实现瀑布流
ajax利用jquery框架实现，每次获取10张图片，每行可以放4张。<br>
主要考虑的是每张图片的宽高不一致，所以需要考虑每列的ul的高度。<br>
实现方法，首先与第一次的ul高度进行比较，然后判断大小，不断重置参照参数。<br>
<strong>具体方法：</strong><br>
let index = 0;<br>
let iHeight = aUl[0].clientHeight;<br>
for (let i = 1,length=aUl.length; i < length; i++) {<br>
      let h = aUl[i].clientHeight;<br>
      if ( h < iHeight ){<br>
               index = i;<br>
               iHeight = h;<br>
              }<br>
         }<br>
