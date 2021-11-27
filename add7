//Задача 7.
//Вариант-4. 
//Дана последовательность натуральных чисел{ Aj }j = 1...n(n <= 10000).
//Удалить из последовательности числа, произведение цифр которых равно 144, а среди оставшихся продублировать числа, содержащие цифру 8.

#include <iostream>
#include <vector>
int proizvedenie(int a)
{
	int b = 1;
	int p = a;
	while (p > 0) {
		b = b * (p % 10);
		p = p / 10;
	}
	return(b);
}

int katya(int a)
{
	int b = 0;
	int p = a;
	while (p > 0)
	{
		if (p % 10 == 8)
		{
			b = 1;
		}
		p = p / 10;
	}
	return(b);
}
int main()
{
	std::vector<int> vec;

	int n;
	int a;
	std::cin >> n;
	for (int i = 0; i < n; i++)
	{
		std::cin >> a;
		vec.push_back(a);
	}

	
	for (int i = 0; i < vec.size(); i++)
	{
		if (proizvedenie(vec[i]) == 144)
		{
			vec.erase(vec.begin() + i);
	
			i = i - 1;
		}
	}

	for (int i = 0; i < vec.size(); i++)
	{
		if (katya(vec[i])== 1)
		{
		
			vec.insert(vec.begin()+i, vec[i]);
				i = i +1;
		}
	}


	for (int i = 0; i < vec.size(); i++)
		std::cout << vec[i] << ' ';

}

