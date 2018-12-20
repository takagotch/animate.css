### animate.css
---
https://github.com/daneden/animate.css/

```sh
npm install animate.css --save
yarn add animate.css

cd path/to/animate.css/
sudo npm install
```

```json
"attention_seekers": {
  "bounce": true,
  "flash": false,
  "pulse": false,
  "shake": true,
  "headShake": true,
  "swing": true,
  "tada": true,
  "wobble": true,
  "jello": true
}

```

```html
<head>
  <link rel="stylesheet" href="animate.min.css">
</head>

<h1 class="animated infinite bounce delay-2s">Example</h1>

<div class="animated bounce faster">Example</div>
```

```css
.yourElement{
  animate-suration: 3s;
  animation-delay: 2s;
  animation-iteration-count: infinite;
}
```

```js
$('#yourElement').addClass('animated bounceOutLeft');

var animationEnd = (function(el){
  var animations = {
    animation: 'animationend',
    OnAnimation: 'onAnimationEnd',
    MozAnimation: 'mozAnimationEnd',
    WebkitAnimation: 'webkitAnimationEnd',
  };
  for(var t in animations){
    if(el.style[t] !== undefined){
      return animations[t];
    }
  }
})(document.createElement('div'));
$('#yourElement').one(animationEnd, doSomething);

$.fn.extend({
  animationCss: function(animationName, callback){
    var animationEnd (function(el){
      var animations = {
        animation: 'animationend',
        OAnimation: 'oAnimationEnd',
        MozAnimation: 'mozAnimationEnd',
        WebkitAnimation: 'webkitAnimationEnd',
      };
      for(var t in animations){
        if(el.style[t] !== undefined){
          return animations[t];
        }
      }
    }
  })(document.createElement('div'));
  this.addClass('animated ' + animationName).one(animationEnd, function(){
    $(this).removeClass( 'animated' + animationName);
    if(typeof callback === 'function') callback();
  });
  return this;
  },
});

$('#yourElement').animateCss('bounce');
$('#yourElement').animateCss('bounce', function(){
});
```

