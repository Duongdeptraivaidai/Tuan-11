# Buổi 1
#### Bài 1
```
# Buổi 2
#### Bài 1(Tách mảng chẵn, lẻ)
```c
#include <iostream>
#include<iomanip>
using namespace std;

int main() {
	int arr[11] = { 1,2,3,4,5,6,7,8,9,10,11 };
	int even[11], odd[11];
	int e, d;

	e = d = 0;

	for (int i = 0; i < 11; i++) {
		if (arr[i] % 2 == 0) {
			even[e] = arr[i];
			e++;
		}
		else {
			odd[d] = arr[i];
			d++;
		}
	}
	cout << "Mang ban dau: ";
	for (int i = 0; i < 11; i++) {
		cout << "a[" << i << "] = " << arr[i] << endl;
	}

	cout << "\n Mang chan la: ";
	for (int i = 0; i < e; i++) {
		cout << even[i] << " ";
	}

	cout << "\nMang le: ";
	for (int i = 0; i < d; i++) {
		cout << odd[i] << " ";
	}
	cout << endl;
}
```
#### Bài 2(Sắp xếp giảm dần)
```c
#include<iostream>
#define MAX 1000
using namespace std;

void HoanVi(int& a, int& b) {
	int temp = a;
	a = b;
	b = temp;
}
int main() {
	int n, arr[MAX];
	cout << "Nhap so luong phan tu: ";
	cin >> n;
	for (int i = 0; i < n; i++)cin >> arr[i];
	for (int i = 0; i < n - 1; i++) {
		for (int j = i + 1; j < n; j++) {
			if (arr[i] < arr[j])HoanVi(arr[i], arr[j]);
		}
	}
	for (int i = 0; i < n; i++)cout << arr[i] << " ";
	cout << endl;	
}
```
#### Bài 3(Sắp xếp số lẻ tăng dần)
```c
#include<iostream>
using namespace std;
const int MAX = 1000;
void HoanVi(int& a, int& b) {
	int temp = a;
	a = b;
	b = temp;
}
int main() {
	int n;
	cin >> n;
	int arr[MAX];
	for (int i = 0; i < n; i++)cin >> arr[i];
	for (int i = 0; i < n - 1; i++) {
		for (int j = i + 1; j < n; j++) {
			if (arr[i] % 2 && arr[j] % 2 && arr[i] > arr[j])HoanVi(arr[i], arr[j]);
		}
	}
	for (int i = 0; i < n; i++)cout << arr[i] << " ";
	return 0;
}
```
#### Bài 4(Sắp xếp số chẵn tăng dần, số lẻ giảm dần)
```c
```
#### Bài 5(Xóa các số lớn nhất)
```c
#include<iostream>
using namespace std;

void XoaSoLonNhat(int arr[], int& n) {
	int max = 0;
	for (int i = 0; i < n; i++) {
		if (arr[i] > arr[max])max = i;
	}
	for (int i = max; i < n; i++) {
		arr[i] = arr[i + 1];
	}
}


int main() {
	int n;
	int arr[100];
	do {
		cout << "Nhap so phan tu: ";
		cin >> n;
	} while (n <= 0 || n > 100);
	for (int i = 0; i < n; i++) {
		cin >> arr[i];
	}
	XoaSoLonNhat(arr, n); 
	cout << "Sau khi xoa so lon nhat: ";
	for (int i = 0; i < n; i++) {
		cout << arr[i] << " ";
	}
}
```
#### Bài 6
```c
```
#### Bài 7(Chèn X vào đầu mảng)
```c
#include<iostream>
using namespace std;
const int s = 1000;
int main() {
	int k = 0;
	int n, x;
	int arr[s];
	cin >> n;
	for (int i = 0; i < n; i++) {
		cin >> arr[i];
	}
	for (int i = n - 1; i >= k; i--) {
		arr[i + 1] = arr[i];
	}
	arr[k] = x;
	++n;
	for (int i = 0; i < n; i++) {
		cout << "a[" << i << "] = " << arr[i];
	}
	return 0;
}
```
