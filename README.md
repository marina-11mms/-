#include <cmath>
#include <iostream>

class Point {
private:
    int x;
    int y;

public:
    Point(int x_coord = 0, int y_coord = 0) : x(x_coord), y(y_coord) {
        std::cout << "Конструктор Point: (" << x << ", " << y << ")" << std::endl;
    }

    ~Point() {
        std::cout << "Деструктор Point: (" << x << ", " << y << ")" << std::endl;
    }

    int getX() const { return x; }
    int getY() const { return y; }
};

int main() {
    Point A(3, 5);
    Point B(7, 2);
    Point C(8, 4);

    float a = sqrt(pow((B.getX() - A.getX()), 2) + pow((B.getY() - A.getY()), 2));
    float b = sqrt(pow((C.getX() - B.getX()), 2) + pow((C.getY() - B.getY()), 2));
    float c = sqrt(pow((A.getX() - C.getX()), 2) + pow((A.getY() - C.getY()), 2)); 
    if (a + b > c && a + c > b && b + c > a) {
        float p = ((a + b + c) / 2);
        float S = sqrt((p * (p - a) * (p - b) * (p - c)));

        printf("%f\n", S);
    } else {
        printf("некоректные данные\n");
    }
    return 0;
}


