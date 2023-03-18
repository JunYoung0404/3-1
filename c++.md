#  오퍼레이터 오버로딩 실습

>  문제

CPnt는 두 지점을 나타내는 클래스 이다.

CPnt p1, p2, p3;

에서 p1의 지점과 p2의 지점이 더해 지는 연산에서

각각의 h와 w가 더해 질 수 있도록

오퍼레이터 오버로딩을 하시오.

>  풀이

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
  
소감 : 심재창교수님께서 과제로 내주신 문제를 수업시간에 배운것을 활용하고 교수님이 참고 하라고 올려주신 코드를 보고 onlinegdb를 이용하여 CRect를CPnt로 바꾼다음 실행해 본 결과 
  각 지점에서 더해지는 코드를 완성시킬수 있었습니다. 또 하지만 깃허브를 완성시키고 보니 <iostream> 이 적용이 안되는것을보고 수정을 눌렀지만 적용은 되어있엇고 표시가 안되는것을
  확인했습니다. 
