---
layout: post
title: 오토매틱 박스조인트
description: 장부가공을 자동으로 해주는 박스조인트 머신
img: /img/portfolio/end12/0.jpg

---


# 2021. 11. 11. 17:04




# m5stack 보드를 베이스로한 박스 조인트 머신이다 

메뉴 구성이 거의 끝났는데, 끝날때쯤에 알고리즘을 잘못 계산해서 다시 한참을 돌아가야 했다.  해당 박스 조인트가공의 변수를 두개 넣었는데 마진 값과 가변 패턴가공이다. 

​

실제 장부날인 12mm날로 가공했을 경우 마진을 0.2mm정도의 작은 값을 주고, 가공 갭을 날의 너비와 같은 12mm로 한다면 굉장히 불필요한 문제가 생긴다. 

​

 음각 가공시 먼저 날 두께인  12mm가공을 하고, 0.2mm이동을 해서, 총 두번 가공을 할 수 밖에 없는데, 실제 이러한 수치는 목공에 무의미한 수치이다. 그럼 일정 수치 이하의 마진 값을 무시해야 하는가의 문제가 생긴다. 일단은 이러한 마진 역시 사용자의 책임이기에 0.1의 마진이든 0.2의 마진이든 마진이 있으면 그 마진 값은 무조건 수용하기로 했다. 

​

 또 하나의 문제는 날 두께가 12mm이고 가공의 갭이 배이상인 24mm 이상이 되는 경우인데, 그렇다면 단순하게 12mm를 두번씩 가공하면 된다고 하지만 실제 그렇게 한다면, 첫번재 날이 깍은 끝부분과 두번째 날이 깍는 시작 부분이 미세하게 떨어질 가능성이 있어 깍이지 않는 문제가 생길 가능성이 있다. 결국에 12mm를 가공하고 11mm를 가공하고 1mm를 가공하는 불필요한 방법을 줄 수 밖에 없다 .

​

​

1. 가공의 갭과 날의 두깨가 같은 경우 

2.가공의 갭과 날의 두깨가 같고, 마진이 있는 경우 

3.가공의 갭과 날의 두깨가 같지는 않지만, 두번째 가공의 경우 날의 너비를 넘지 않는 경우 

4. 가공의 갭과 날의 두깨가 같지는 않고, 두번째 가공의 경우 날의 너비를 넘지는 않지만, 마진의 값에 의해서 날의 너비를 넘어 버리는 경우 

5.날의 너비 2배이상의 갭인 경우. 서로 맞닿은 부분의 문제. 

6. 5번과  4번의 경우와 3번의 경우가 겹치는 경우. 

​

 가공이 반복되기에 패턴의 수가 많아 지면 이 경우의 수가 꼬이지 않게 해야 한다 .

​

작동 영상 링크 
https://blog.naver.com/hangmini12/222565220217




<div class="img_row">
<img class="col two" src="{{ site.baseurl }} /img/portfolio/end12/11.jpg" alt="" title="example image"/>

</div>

<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/0.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/2.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/3.jpg" alt="" title="example image"/>
	</div>	


<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/4.png" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/6.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/7.jpg" alt="" title="example image"/>
	</div>	

<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/8.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/12.png" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end12/13.png" alt="" title="example image"/>
	</div>	


----------
나머지 링크 

https://blog.naver.com/hangmini12

등등
