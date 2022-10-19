# DEMO HINH CHU NHAT
## KHAI BAO
#include <iostream>

using namespace std;

class ChuNhat
{
private:
    double chieudai, chieurong;

public:
    void nhap();
    void xuat();
    double chuvi();
    void sosanh(ChuNhat a);
    bool kiemtra();
};
## HAM NHAP
void ChuNhat::nhap()
{
    cout << "Nhap chieu dai: ";
    cin >> chieudai;
    cout << "Nhap chieu rong: ";
    cin >> chieurong;
}
## HAM XUAT
void ChuNhat::xuat()
{
    cout << "co kich thuoc " << chieudai << " x " << chieurong << endl;
}
## HAM TINH CHU VI
double ChuNhat::chuvi()
{
    double P = (chieudai + chieurong)*2;
    return P;
}
## HAM SO SANH
void ChuNhat::sosanh(ChuNhat a)
{
    if (chuvi() > a.chuvi())
        cout << "Chu vi hinh chu nhat thu nhat lon hon hinh chu nhat thu hai" << endl;
    else if (chuvi() == a.chuvi())
        cout << "Chu vi hinh chu nhat thu nhat bang hinh chu nhat thu hai" << endl;
    else
        cout << "Chu vi hinh chu nhat thu nhat nho hon hinh chu nhat thu hai" << endl;
}
## HAM KIEM TRA
bool ChuNhat::kiemtra()
{
    if (chieudai == chieurong)
        return true;
    else
        return false;
}

## HAM MAIN
int main()
{
    ChuNhat a, b;
    cout << "Nhap hinh chu nhat thu nhat: " << endl;
    a.nhap();
    cout << "Nhap hinh chu nhat thu hai: " << endl;
    b.nhap();

    cout << "\nHinh chu nhat thu nhat ";
    a.xuat();
    cout << "Hinh chu nhat thu hai ";
    b.xuat();

    cout << "\nChu vi hinh chu nhat thu nhat la " << a.chuvi() << endl;
    cout << "Chu vi hinh chu nhat thu hai la " << b.chuvi() << endl << endl;

    a.sosanh(b);

    cout << "\nHinh chu nhat la hinh vuong: " << a.kiemtra() << endl;
    cout << "Hinh chu nhat la hinh vuong: " << b.kiemtra() << endl;

    return 0;
}
