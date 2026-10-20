# Zmuszenie CMake do korzystania przynajmniej z wersji 1.12
# Jeżeli ktoś ma zainstalowaną starszą - program nie zadziała
cmake_minimum_required(VERSION 3.12)

# Nazwa całego projektu (może być tylko jedna)
project(PWDP-Michna)

# Ustawienie wersji kompilatora C++ na C++20 by działał std::format
# std::print wymaga C++23 oraz dopisania innych linijek
set(CMAKE_CXX_STANDARD 20)

# Zmuszenie kompilatora do korzystania z powyższago C++
# Jeżeli ktoś takiego nie ma, projekt się nie włączy
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Dodaje folderu o nazwie "lista1"
# Tam znajdują się pliki z listy 1
# W tym folderze musi znajdować się inny plik CMakeLists.txt, który konfiguruje folder 
add_subdirectory("lista1")
add_subdirectory("lista2")