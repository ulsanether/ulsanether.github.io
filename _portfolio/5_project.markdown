---
layout: post
title: grbl2 co2레이져
description: grbl과 grbl2방식 레이저 커터와 옥토프린터 
img: /img/portfolio/end06/1.jpg

---


# 2019. 12. 10. 13:46

grbl2 방식의 co2레이저 커터이다. 

보드는 mks sbase 1.3v  (스무디웨어 보드)

 일단 주문 한 보드이다. co2 자작을 하는 상당수가 이 보드나 스무디웨어의 펌웨어를 쓰는 보드로 구성을 하고 있었다. 상대적으로 낮은 가격, 높은 성능, 호환성, 거기다 많은 드라이버 구성이 있다. 완벽히 laser 구성으로 나온 것이 아니지만, 스무디웨어는 전천후로 많이 쓰는 보드중 하나이다. 단점과 장점은 이제곧 알 수가 있을것 같다. 

<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end06/13.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end06/14.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end06/15.jpg" alt="" title="example image"/>
		
</div>

$10=0 ;send work coordinates in statusReport (needed for LW4!)

$3=3 ;invert X and Y stepper direction

$5=1 ;endstopps are NC (normaly closed)

$22=1 ;activate homing

$23=1 ;homing in X- and Y+ direction

$30=1000 ;max. S-value for Laser-PWM

$31=0 ;min. S-value

$32=1 ;Laser Mode on

$33=5000 ;PWM frequency 5000 Hz (lower = better grayscale, higher = better cut)

$100=160 ;steps/mm in X, depending on your pulleys and microsteps

$101=160 ;steps/mm in Y, depending on your pulleys and microsteps

$102=160 ;steps/mm in Z, depending on your pulleys and microsteps

$110=24000 ;max. rate mm/min in X, depending on your system

$111=24000 ;max. rate mm/min in Y, depending on your system

$112=24000 ;max. rate mm/min in Z, depending on your system

$120=2500 ;acceleration mm/s^2 in X, depending on your system

$121=2500 ;acceleration mm/s^2 in Y, depending on your system

$122=2500 ;acceleration mm/s^2 in Z, depending on your system

$130=600 ;max. travel mm in X, depending on your system

$131=300 ;max. travel mm in Y, depending on your system

$132=50 ;max. travel mm in Z, depending on your system

$140=0.6 ;X stepper current 0.4A

$141=0.6 ;Y stepper current 0.6A

$142=0.0 ;Z stepper current 0.0A



# 2019. 11. 9. 1:36


co2용 cnc쉴드와 옥토프린터를 시험해 봤다. 간단한 테스트만 하고 일단 패스를 해야 겠다. mks sbase 1.3v 의 보드를 주문을 했는데, 가격이 생각보다 세다. skr 1.3 보드가 상대적으로 훨 싼데, 핀아웃 문제 때문에 grbl-lpc가 동작 하지 않는다고 한다. mks gen은 8비트라 안되고...


그리고 sbase 1.3에는 스태퍼 전류를 조절 하는 I2C Chip이 있고, 이 칩의 지원 여부는 보드의 점퍼를 보고'지원 가능성'을 유추 할 수가 있다.

<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end06/2.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end06/3.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end06/4.jpg" alt="" title="example image"/>
		
</div>

간단한 옥토 프린터 화면이다. 별 건 없다. 동작도 별건 없다. 끝

<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end06/5.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end06/6.jpg" alt="" title="example image"/>

		
</div>
<br/>

# 2019. 11. 6. 11:30


컨피그를 다시 수정했다. 속도가 너무 느리다. 그리고 모터 핀설정이 잘못 되었는지 소음이 있다. 엑셀 값을 올리니까 진동이 너무 심하고, 이것 저것 손볼 것이 몇가지 있는것 같다. 

​

<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/7.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/8.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/9.jpg" alt="" title="example image"/>
</div>


2019/11/06 11:26:46 - $2=0

2019/11/06 11:26:46 - $3=0

2019/11/06 11:26:46 - $4=0

2019/11/06 11:26:46 - $5=0

2019/11/06 11:26:46 - $6=0

2019/11/06 11:26:46 - $10=3

2019/11/06 11:26:46 - $11=0.010

2019/11/06 11:26:46 - $12=0.002

2019/11/06 11:26:46 - $13=0

2019/11/06 11:26:46 - $20=0

2019/11/06 11:26:46 - $21=0

2019/11/06 11:26:46 - $22=0

2019/11/06 11:26:46 - $23=0

2019/11/06 11:26:46 - $24=25.000

2019/11/06 11:26:46 - $25=500.000

2019/11/06 11:26:46 - $26=250

2019/11/06 11:26:46 - $27=1.000

2019/11/06 11:26:46 - $30=1000

2019/11/06 11:26:46 - $31=0

2019/11/06 11:26:46 - $32=0

2019/11/06 11:26:46 - $100=250.000

2019/11/06 11:26:46 - $101=250.000

2019/11/06 11:26:46 - $102=250.000

2019/11/06 11:26:46 - $110=10000.000

2019/11/06 11:26:46 - $111=10000.000

2019/11/06 11:26:46 - $112=500.000

2019/11/06 11:26:46 - $120=500.000

2019/11/06 11:26:46 - $121=500.000

2019/11/06 11:26:46 - $122=500.000

2019/11/06 11:26:46 - $130=300.000

2019/11/06 11:26:46 - $131=200.000

2019/11/06 11:26:46 - $132=200.000


<br/>






# 2019. 11. 6. 3:01
   


 중국산 CO2 LASER보드에는 좀 비싸고 더 좋은 루다(RUDA) 저가의 NANO M2보드가 있습니다. 
제가 중고로 업어온 레이저 컷터에는 M2보드가 있었고, 이 보드는 근본적으로 하자가 많이 있었습니다.



1.컴퓨터의 연결이 필수여야 하며, 연결에 문제가 많습니다. 
2. 코렐레이져라는 전용 프로그램과 키 락이 필수여야 합니다. 하지만 전용 프로그램과 키락이 문제가 많습니다.  k40 whisperer라는 프로그램을 쓸 수는 있습니다.



 어쨌거나, 보드를 교체해보자고 생각하고, 남아 도는 CNC쉴드로 교체를 해 보려 했습니다. 가능 할 거라 생각했지만, 실행하기 까지 시간이 좀 필요 했습니다. 가장 큰 이유는 전에 사용자 분이 기존의 연결 선들을 굵은 선으로 바꿔 버려서, 선 색도 알 수가 없고, 그걸 일일이 더듬어 다시 배치해 연결하기가 귀찮았습니다. 두번 째는 k40 whisperer 프로그램에 익숙해 져서 굳이 바꿔야 할 필요성을 못 느껴서 그렇습니다. 제 목표는 CO2의 자작이었기에, 다시 건들어 봤습니다. 이 기록이 도움이 되기를 바랍니다. 


</div>
 
<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/5.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/6.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/9.jpg" alt="" title="example image"/>


</div>
 
<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/10.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/11.png" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/12.jpg" alt="" title="example image"/>


</div>
 
<div class="img_row">
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/13.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/14.jpg" alt="" title="example image"/>
<img class="col one" src="{{ site.baseurl }} /img/portfolio/end05/15.jpg" alt="" title="example image"/>

</div>
----
<br/>

# 나머지 기록 링크 

https://blog.naver.com/hangmini12/221321429600

https://blog.naver.com/hangmini12/221321132828

https://blog.naver.com/hangmini12/221310086811

https://blog.naver.com/hangmini12/221306230471