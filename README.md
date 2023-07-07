 #include <iostream>
#include <vector>

std::vector<int> encontrarFactores(int n) {
    std::vector<int> factores;
    for (int i = 1; i <= n; i++) {
        if (n % i == 0) {
            factores.push_back(i);
        }
    }
    return factores;
}

int main() {
    int numero;

    std::cout << "Ingrese el numero que quiere factorizar: ";
    std::cin >> numero;

    std::vector<int> vectorFactores = encontrarFactores(numero);
    std::cout << "VectorFactores: ";
    for (int i = 0; i < vectorFactores.size(); i++) {
        std::cout << vectorFactores[i] << " ";
    }
    std::cout << std::endl;

    return 0;
}
