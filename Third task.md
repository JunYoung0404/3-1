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



소감:
