#include <iostream>
using namespace std;

int partition(int* arr, int start, int size)
{

	int p = start;
	size_t i = start;
	int	sizeM = size - 1;
	for (; i < sizeM; i++)
	{
		if (arr[i] < arr[sizeM])
		{
			swap(arr[p], arr[i]);
			p++;
		}
	}
	swap(arr[sizeM], arr[p]);
	return p;
}

void my_quik_sort(int* arr, int size)
{
	int* stack = new int[size];
	stack[0] = 0;
	stack[1] = size;
	int top = 1;
	int start, end, piv;
	while (top > 0)
	{
		end = stack[top--];
		start = stack[top--];
		piv = partition(arr, start, end);
		if (piv > start + 1)
		{
			stack[++top] = start;
			stack[++top] = piv ;
		}
		if (piv < end - 1)
		{
			stack[++top] = piv + 1;
			stack[++top] = end;
		}


	}

	delete stack;
}

void main()
{
	int arr[] = { 9,12,34,2,1,-7,344,11,2,-4,22,3};
	my_quik_sort(arr, sizeof(arr) / 4);
	for (size_t i = 0; i < sizeof(arr) / 4; i++)
	{
		cout << arr[i] << "  ";
	}

	system("pause");
}



