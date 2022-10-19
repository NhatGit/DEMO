# DEMO HINH CHU NHAT
## KHAI BAO
- Khai bao thuoc tinh (private), phuong thuc (public) <br />
#include <iostream> <br />

using namespace std; <br />

class ChuNhat 
{<br />
private:
    double chieudai, chieurong;<br />

public:<br />
    void nhap();
    void xuat();
    double chuvi();
    void sosanh(ChuNhat a);
    bool kiemtra();<br />
};<br />
## HAM NHAP
void ChuNhat::nhap()
{<br />
    cout << "Nhap chieu dai: ";
    cin >> chieudai;<br />
    cout << "Nhap chieu rong: ";
    cin >> chieurong;
}<br />
## HAM XUAT
void ChuNhat::xuat()
{<br />
    cout << "co kich thuoc " << chieudai << " x " << chieurong << endl;
}<br />
## HAM TINH CHU VI
double ChuNhat::chuvi()
{<br />
    double P = (chieudai + chieurong)*2;<br />
    return P;
}<br />
## HAM SO SANH
void ChuNhat::sosanh(ChuNhat a)
{<br />
    if (chuvi() > a.chuvi())
        cout << "Chu vi hinh chu nhat thu nhat lon hon hinh chu nhat thu hai" << endl;<br />
    else if (chuvi() == a.chuvi())
        cout << "Chu vi hinh chu nhat thu nhat bang hinh chu nhat thu hai" << endl;<br />
    else
        cout << "Chu vi hinh chu nhat thu nhat nho hon hinh chu nhat thu hai" << endl;
}<br />
## HAM KIEM TRA
bool ChuNhat::kiemtra()
{<br />
    if (chieudai == chieurong)
        return true;<br />
    else
        return false;
}<br />

## HAM MAIN
int main()
{<br />
    ChuNhat a, b;<br />
    cout << "Nhap hinh chu nhat thu nhat: " << endl;
    a.nhap();<br />
    cout << "Nhap hinh chu nhat thu hai: " << endl;
    b.nhap();<br />

    cout << "\nHinh chu nhat thu nhat ";
    a.xuat();<br />
    cout << "Hinh chu nhat thu hai ";
    b.xuat();<br />

    cout << "\nChu vi hinh chu nhat thu nhat la " << a.chuvi() << endl;<br />
    cout << "Chu vi hinh chu nhat thu hai la " << b.chuvi() << endl << endl;<br />

    a.sosanh(b);<br />

    cout << "\nHinh chu nhat la hinh vuong: " << a.kiemtra() << endl;<br />
    cout << "Hinh chu nhat la hinh vuong: " << b.kiemtra() << endl;<br />

    return 0;
}
