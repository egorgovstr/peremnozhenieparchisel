#include <iostream>
#include <vector>

int main() {
    // Запрос у пользователя количества пар чисел
    std::cout << "Введите количество пар чисел: ";
    int numPairs;
    std::cin >> numPairs;

    // Вектор для хранения чисел
    std::vector<std::pair<int, int>> pairs;

    // Ввод пар чисел от пользователя
    for (int i = 0; i < numPairs; ++i) {
        int num1, num2;
        std::cout << "Введите первое и второе число для пары " << i + 1 << ": ";
        std::cin >> num1 >> num2;
        pairs.push_back(std::make_pair(num1, num2));
    }

    // Перемножение пар чисел
    std::cout << "Результат перемножения пар чисел:\n";
    for (const auto& pair : pairs) {
        int result = pair.first * pair.second;
        std::cout << pair.first << " * " << pair.second << " = " << result << "\n";
    }

    return 0;
}
