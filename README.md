# Практика
Мой первый репозиторий
#include <iostream>
#include <vector>

using namespace std;

int main() 
{
  vector<double> x = {0, 1, 2, 3, 4}; // Заданные значения x
  int n = x.size();   // Количество элементов
  vector<double> y(n); // Вектор для хранения значений y
  cout << "Введите " << n << " значений y:" << endl; // Ввод значений y от пользователя
  for (int i = 0; i < n; ++i) 
  {
    cin >> y[i];
  }
  double sumX = 0, sumY = 0, sumXY = 0, sumX2 = 0; // Вычисление необходимых сумм
  for (int i = 0; i < n; ++i) {
    sumX += x[i];
    sumY += y[i];
    sumXY += x[i] * y[i];
    sumX2 += x[i] * x[i];
  }
  double a = (n * sumXY - sumX * sumY) / (n * sumX2 - sumX * sumX); // Вычисление коэффициентов a и b
  double b = (sumY - a * sumX) / n;
  cout << "Аппроксимация: y = " << a << "x + " << b << endl;
  return 0;
}


