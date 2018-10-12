## 实现一个多视频拼接成长视频
var ctx = [{img_url: "img/c1.png"},{img_url: "img/c2.png"},{img_url:"http://vjs.zencdn.net/v/oceans.mp4"},{img_url: "img/c3.png"}];
var dur =[{time:"1000"},{time:"3000"},{time:"4000"},{time:"3000"}]
sum(0,dur,ctx);
function sum(i,arr,arr2){
i++;
if(i>arr.length){
return 
}else{
console.log("这里你的渲染",arr2[i-1])

setTimeout(function(){
sum(i,arr,arr2);
},parseInt(arr[i-1].time))

}
}
