#  복습과제
>1. friend를 활용하는 [클래스]의 예를 하나 만드시오.
```
#include <iostream> 
using namespace std;
class Jun {
  	int x;
  public:
    Jun(int a=10):x(a){}
    friend int main();
};
int main () {
    Jun r;
    cout << r.x << endl;
    return 0;
}
```

>2. [클래스]에서 static을 활용하는 예를 하나 보이시오.
```
#include <iostream>
using namespace std;
class Jun {
public:
    static int jun;
    void po() { jun++; }
};
int Jun::jun=0;
int main() {
    Jun c;
    c.po();
    c.po();
    c.po();
    c.po();
    cout << "물건 갯수: "  <<Jun::jun << "개 " <<  endl;
    return 0;
}
```
>3. CPoly로 부터 w, h를 상속받고,사각형의 면적을 구하는 코딩을 하시오. 포인터를 활용하여 화면에 출력하시오.
```
#include<iostream>
using namespace std;
class CPoly{
protected:
	int w, h;
};
class CRect : public CPoly{
public:
	CRect(){ w=5; h=4;}
	int Area(){cout << w*h;	}
};
int main(){
	CRect v;
	CRect* p = &v;
	p->Area();
	
}
```
출력결과:
![깃허브 올릿것](https://user-images.githubusercontent.com/50895748/227857144-4ffec7a5-97ec-4c8b-ab13-734028607377.png)

# 소감:
이번 과제를 하면서 static에 대해 더 자세히 알게 되었고 friend 라는것은 처음들어보았는데 아직까지는 익숙하지 않지만 계속 반복숙달 하면 완전히 제것이 될수있을것 같습니다. 그리고 상속과 포인터는 조금 헷갈렸지만 이번에 교수님께서 카페에 올려주신것과 수업시간에 가르쳐 주신것을 토대로 다시 복습해보니 이해가 쉽게 되는것 같았습니다. 벌써 1달 동안 많은걸 배운것 같습니다. 매일 복습하고 모르는것은 교수님과 친구들 또 chatgpt를 통해서 다시 배우며 남은 중간고사 떄 까지 열심히 공부하여 A이상의 성적을 받도록 하겠습니다.
