<!--- KAYNAK: http://www.kodbul.org --->
<script language="JavaScript"> 
NS4=(document.layers);
IE4=(document.all);
Clrs=new Array('ff0000','00ff00','ffffff','ff00ff','ffa500','ffff00','00ff00','ffffff','ff00ff')
yBase=0;
xBase=0;
step=3;
currStep=0;
Ypos=0;
Xpos=0;
if (NS4){
for (i=0; i < 14; i++)
document.write('<LAYER NAME="n'+i+'" LEFT=0 TOP=0 CLIP="0,0,'+i/4+','+i/4+'"></LAYER>');
window.captureEvents(Event.MOUSEMOVE);
  function nMouse(evnt){
Ypos = evnt.pageY-window.pageYOffset;
Xpos = evnt.pageX;
}
window.onMouseMove=nMouse;
}
if (IE4){
document.write('<div id="e" style="position:absolute;top:0;left:0"><div style="position:relative">');
for (i=0; i < 14; i++)
{document.write('<div id="me" style="position:absolute;top:0;left:0;width:'+i/4+';height:'+i/4+';font-size:'+i/4+'"></div>')}
document.write('</div></div>');
function iMouse(){
Ypos=event.y;
Xpos=event.x;
}
document.onmousemove = iMouse;
}
function Comet(){
S=(NS4)?window.pageYOffset:0;
if (IE4) e.style.top=document.body.scrollTop;
var yBase=(document.layers)?window.innerHeight/4:window.document.body.clientHeight/4;
var xBase=(document.layers)?window.innerWidth/4:window.document.body.clientWidth/4;
for (i=0; i < 14; i++){
var randCol=Math.round(Math.random()*8);
var layer=(NS4)?document.layers['n'+i]:me[i].style;
layer.top =Ypos + yBase*Math.cos((currStep+i*4)/12)*Math.cos(0.7+currStep/200)+S;
layer.left=Xpos + xBase*Math.sin((currStep+i*3)/10)*Math.sin(8.2+currStep/400);
if (NS4) layer.bgColor=Clrs[randCol];
if (IE4)layer.background=Clrs[randCol];
}
currStep+=step;
setTimeout("Comet()",40);
}
window.onload=Comet;
</script>
<!--- KAYNAK: http://www.kodbul.org --->
