#define _CRT_SECURE_NO_WARNINGS 1
#include<iostream>
using namespace std;

#include<assert.h>

void Print(int* a, int size)
{
	for (int i = 0; i < size; i++)
	{
		cout << a[i] << "  ";
	}
	cout << endl;
}


void QuickSort(int* a, int left,int right)
 {
	assert(a);
	int low = left;
	int high = right;
	int key = a[low];

	while (low < high)
	{				
		while (low < high && key <= a[high])
		{
			high--;
		}
		a[low] = a[high];

		while (low <high && key >= a[low])
		{
			low++;
		}
		a[high] = a[low];
	}
	a[low] = key;

	if (left <= high)
	{
		QuickSort(a, left, low - 1);
		QuickSort(a, low + 1, right);
	}
	
}


void TestQuickSort()
{
	int a[14] = { 0, 5,0,0, 8, 6,6, 3, 7,5, 2, 4, 1, 9 };
	QuickSort(a,0, sizeof(a) / sizeof(a[0])-1);
	Print(a, sizeof(a) / sizeof(a[0]));
}


int main()
{
	TestQuickSort();
	system("pause");
	return 0;
}
