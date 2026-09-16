#include<iostream>
using namespace std;

class mang1chieu
{
private:
    int a[100];
    int n;

public:
    void nhap();
    void xuat();
    int timkiem(int x);
    void sapxep();
    void xoa(int k);
};

void mang1chieu::nhap()
{
    cout << "Nhap so phan tu n = ";
    cin >> n;

    for (int i = 0; i < n; i++)
    {
        cout << "a[" << i << "] = ";
        cin >> a[i];
    }
}
void mang1chieu::xuat()
{
    for (int i = 0; i < n; i++)
    {
        cout << a[i] << " ";
    }
}

int main()
{
    int x, k;
    mang1chieu m;

    m.nhap();

    cout << "Mang vua nhap: ";
    m.xuat();

    cout << "\nNhap gia tri can tim x = ";
    cin >> x;

    k = m.timkiem(x);

    if (k == -1)
    {
        cout << "Khong tim thay " << x;
    }
    else
    {
        cout << "Tim thay " << x
             << " tai vi tri " << k;
    }

    m.sapxep();

    cout << "\nMang sau khi sap xep la: ";
    m.xuat();

    cout << "\nNhap vi tri can xoa k = ";
    cin >> k;

    m.xoa(k);

    cout << "\nMang sau khi xoa: ";
    m.xuat();

    return 0;
}
