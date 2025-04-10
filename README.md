Structura Proiectului
Rolul principal al fișierelor componente:
point.cpp și point.hpp

Funcționalitate: Administrează pozițiile (coordonatele) folosite pentru localizarea șarpelui și a celorlalte obiecte din joc.

Notă: Codul este compilat sub forma unei biblioteci statice – libpoint.a.

board.cpp și board.hpp

Funcționalitate: Definește dimensiunile grilei de joc și oferă suport pentru plasarea obiectelor.

Notă: Aceste fișiere sunt transformate într-o bibliotecă statică – libboard.a.

snake.cpp și snake.hpp

Funcționalitate: Gestionează comportamentul șarpelui – deplasarea, extinderea și verificarea coliziunilor.

Notă: Se compilează într-o bibliotecă statică – libsnake.a.

painter.cpp și painter.hpp

Funcționalitate: Se ocupă cu desenarea graficii și afișarea textelor pe tablă.

Notă: Utilizează STL (std::vector<std::string>) pentru reprezentări vizuale și este compilat într-o bibliotecă statică – libpainter.a.

abstract_painter.hpp

Funcționalitate: Reprezintă o interfață abstractă pentru partea grafică a jocului, implementată ulterior de Painter.

Notă: Codul a fost adaptat pentru a folosi STL (std::vector, std::string) pentru o mai bună siguranță și flexibilitate.

.gitignore

Funcționalitate: Exclude din versiunea finală fișierele temporare generate în timpul compilării, precum:

Fișiere obiect (*.o)

Biblioteci (*.a, *.so)

Executabile (*.exe, *.out)

Makefile

Funcționalitate: Coordonează procesul de construire a aplicației.

Modificări:

Fiecare modul (Point, Board, Painter, Snake) este compilat individual în biblioteci statice.

Conține reguli pentru compilare, curățare și integrarea componentelor.

main.cpp

Funcționalitate: Reprezintă punctul de pornire al aplicației, în care sunt reunite toate modulele și este definit comportamentul jocului.

Detalii Tehnice și Dependențe
Mediu de dezvoltare:

Compilator: g++, compatibil cu standardul C++17

Sistem de operare: Linux, Windows, macOS

Biblioteci utilizate:

STL (<vector>, <string>)

iostream pentru intrare/ieșire

Dependențe externe:

Nu sunt necesare biblioteci din surse externe

Pași pentru Construirea și Rularea Jocului
Clonarea proiectului din depozitul Git:

bash
Копировать
Редактировать
git clone <repository_url>
cd SnakeGame
