# DZ_5_3 (Двумерный массив)

// Вывод массива на экран.cpp : Этот файл содержит функцию "main". Здесь начинается и заканчивается выполнение программы.
//

#include <iostream>
#include <string>
using namespace std;

int main()
{
  setlocale(LC_ALL, "Russian");

  const int rows = 3, columns = 6;

  int arr[rows][columns] =
  {
    {1, 2, 3, 4, 5, 6},
    {7, 8, 9, 10, 11, 80},
    {13, 14, 55, 16, 17, 18}
  };

  int min = arr[0][0];
  int max = arr[0][0];

  int min_i = 0, min_j = 0;
  int max_i = 0, max_j = 0;

  cout << "Массив:";

  for (int i = 0; i < rows; i++)
  {
    for (int j = 0; j < columns; j++)
    {      
      if (arr[i][j] < min)
      {
        min = arr[i][j];
        min_i = i;
        min_j = j;
      }

      if (arr[i][j] > max)
      {
        max = arr[i][j];
        max_i = i;
        max_j = j;

      }
    }

  }
  cout << '\n' << endl;


  for (int row{}; row < rows; row++)
  {
    for (int column{}; column < columns; column++)
    {
      cout << arr[row][column] << '\t';
    }
    cout << endl;
  }

  cout << '\n' << endl;

  cout << "Индекс минимального элемента: " << min_i << min_j << '\n' << endl;
  cout << "Индекс максимального элемента: " << max_i << max_j << endl;

  return 0;
}
