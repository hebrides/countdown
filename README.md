countdown
=========

Did this for a site effect. It's as basic as it can get :-)

```
<!doctype html>  
<html>  
<head>  
<meta charset="UTF-8">  
<title>Countdown</title>  
</head>  
<body>  
<div>  
  <p>Countdown</p>
  <p id='countdown'>&nbsp;</p>
</div>  
</body>  
<script>  
setInterval(function() {showCountdown()},1000);  
var goal = new Date(2015, 0, 24, 18, 0, 0, 0);  
function showCountdown() {  
 var current = new Date();
 var timeLeft = goal-current;
 var days = timeLeft/(86400000);
 var hours = (days % 1)*24;
 var minutes = (hours % 1)*60;
 var seconds = (minutes % 1)*60;
 var mils = (seconds % 1)*1000;

 document.getElementById('countdown').innerHTML
      = Math.floor(days)+' days '
      +Math.floor(hours)+' hours '
      +Math.floor(minutes)+' minutes '
      +Math.floor(seconds)+' seconds'; 
}
</script>  
</html>  
```


