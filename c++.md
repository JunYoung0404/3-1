#  오퍼레이터 오버로딩 실습

>  문제

CPnt는 두 지점을 나타내는 클래스 이다.

CPnt p1, p2, p3;

에서 p1의 지점과 p2의 지점이 더해 지는 연산에서

각각의 h와 w가 더해 질 수 있도록

오퍼레이터 오버로딩을 하시오.

>  풀이
```
#include<iostream>

using namespace std;

class CPnt

{

  int w, h;

public:

 CPnt(int _w, int _h){ w=_w; h=_h; }

 CPnt(){w=0;h=0;}


 void Pr ()  { cout << w << ' ' << h << '\n'; }

 

  CPnt operator+(CPnt r){

  CPnt k;
  
  k.w = w + r.w;
  k.h = h + r.h;
  return(k);

  }

};

int main ()

{

  CPnt p1(2, 1), p2(3,2), p3;



  p3 = p1 + p2;

  p3.Pr ();


  return 0;

}
```
  
#  소감 
심재찬 교수님께서 과제로 내주신 문제를 수업 시간에 배운 것을 활용하고 교수님이 참고하라고 올려주신 코드를 보고 onlinegdb를 이용하여 CRect를 CPnt로 바꾼 다음 실행해 본 결과
각 지점에서 더해지는 코드를 완성시킬 수 있었습니다. 
깃허브를 오랜만에 사용해 보았는데 다시 열심히 잔디밭을 채워나가야 할 것 같습니다. 또한 깃허브와 노선을 열심히 사용하여
깃허브와 노선의 전문가가 되고 싶습니다. 교수님께서 수업 시간에 알려주신 것을 눈으로 보기만 해서는 안되고 직접 손으로 쓰면서 외우면 잘 외워지는 것 같습니다. 또한 chatGPT를
열심히 사용하여 더 많은 지식을 얻고 싶습니다.
앞으로 교수님과 chatGPT의 도움을 열심히 받아 C++과 코딩을 즐겁게 할 것입니다.
