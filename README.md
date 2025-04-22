#include <cmath>
#include <iostream>
struct point{
int x;
int y;
};
int main()
{
    point A;
    A.x=9;
    A.y=5;
    
    point B;
    B.x=4;
    B.y=6;
    
    point C;
    C.x=3;
    C.y=6;
    
    float a=sqrt(pow((B.x-A.x),2)+pow((B.y-A.y),2));
    float b=sqrt(pow((C.x-B.x),2)+pow((C.y-B.y),2));
    float c=sqrt(pow((A.x-B.x),2)+pow((A.y-C.y),2));
    
    
    if (a+b>c && a+c>b && b+c>a)
    {
        float p=((a+b+c)/2);
        float S=sqrt((p*(p-a)*(p-b)*(p-c)));
    
        printf ("%f\n", S);
    }
    else { 
        printf ("некоректные данные");
    }
    return 0;
}
