---
layout: default
---

<body>
  <div class="index-wrapper">
    <div class="aside">
      <div class="info-card">
        <h1>会飞的鱼</h1>
        <a href="https://weibo.com/u/1837358905/" target="_blank"><img src="http://www.weibo.com/favicon.ico" alt="" width="25"/></a>
        <a href="https://www.douban.com/people/80391599/" target="_blank"><img src="http://www.douban.com/favicon.ico" alt="" width="22"/></a>
        <a href="http://instagram.com/beiyuu/" target="_blank"><img src="http://d36xtkk24g8jdx.cloudfront.net/bluebar/00c6602/images/ico/favicon.ico" alt="" width="22"/></a>
      </div>
      <div id="particles-js"></div>
    </div>

    <div class="index-content">
      <ul class="artical-list">
        {% for post in site.categories.blog %}
        <li>
          <a href="{{ post.url }}" class="title">{{ post.title }}</a>
          <div class="title-desc">{{ post.description }}</div>
        </li>
        {% endfor %}
      </ul>
    </div>
  </div>
 <!--  <embed type="application/x-shockwave-flash" src="http://cdn.abowman.com/widgets/pendulumclock/pendulumClockV2.swf" width="280" height="210" id="flashID" name="flashID" bgcolor="#FFFFFF" quality="high" flashvars="up_backgroundColor=FFFFFF" wmode="opaque" allowscriptaccess="always" style="position: absolute;right: 30px;top:100px"> -->
    <object type="application/x-shockwave-flash" style="outline:none;" data="http://cdn.abowman.com/widgets/pendulumclock/pendulumClockV2.swf?up_hourOffset=0&up_pendulumColor=FFFFFF&up_clockName=Pendulum%20Clock&up_minOffset=0&up_logoText=zxwj&up_quarterChime=0&up_handColor=000000&up_faceColor=FFFFFF&up_tick=0&up_backgroundColor=FFFFFF&up_numberColor=808080&up_quarterTilChime=0&up_hourChime=0&up_halfChime=0&up_lineColor=808080&" width="300" height="200"><param name="movie" value="http://cdn.abowman.com/widgets/pendulumclock/pendulumClockV2.swf?up_hourOffset=0&up_pendulumColor=FFFFFF&up_clockName=Pendulum%20Clock&up_minOffset=0&up_logoText=zxwj&up_quarterChime=0&up_handColor=000000&up_faceColor=FFFFFF&up_tick=0&up_backgroundColor=FFFFFF&up_numberColor=808080&up_quarterTilChime=0&up_hourChime=0&up_halfChime=0&up_lineColor=808080&"></param><param name="AllowScriptAccess" value="always"></param><param name="wmode" value="opaque"></param><param name="bgcolor" value="FFFFFF"/></object>
  <script src="js/particles.min.js" type="text/javascript"></script>
  <script>
    particlesJS("particles-js", {"particles":{"number":{"value":160,"density":{"enable":true,"value_area":800}},"color":{"value":"#ffffff"},"shape":{"type":"circle","stroke":{"width":0,"color":"#000000"},"polygon":{"nb_sides":5},"image":{"src":"img/github.svg","width":100,"height":100}},"opacity":{"value":1,"random":true,"anim":{"enable":true,"speed":1,"opacity_min":0,"sync":false}},"size":{"value":3,"random":true,"anim":{"enable":false,"speed":4,"size_min":0.3,"sync":false}},"line_linked":{"enable":true,"distance":150,"color":"#ffffff","opacity":0.4,"width":1},"move":{"enable":true,"speed":1,"direction":"none","random":true,"straight":false,"out_mode":"out","bounce":false,"attract":{"enable":false,"rotateX":600,"rotateY":600}}},"interactivity":{"detect_on":"canvas","events":{"onhover":{"enable":true,"mode":"bubble"},"onclick":{"enable":true,"mode":"repulse"},"resize":true},"modes":{"grab":{"distance":400,"line_linked":{"opacity":1}},"bubble":{"distance":250,"size":0,"duration":2,"opacity":0,"speed":3},"repulse":{"distance":400,"duration":0.4},"push":{"particles_nb":4},"remove":{"particles_nb":2}}},"retina_detect":true})
  </script>
</body>
