# Тестовое задание -> геометрическими кривыми в трехмерном пространстве  (Test_task_CADEX)

## 1. Описание
Проект представляет собой набор классов для работы с геометрическими кривыми в трехмерном пространстве. Реализованы классы для кругов, эллипсов и 3D-спиралей, а также функции для генерации случайных объектов и их обработки.

## 2. Цель проекта
Цель проекта - предоставить удобный и расширяемый инструмент для работы с геометрическими кривыми. Каждый класс обеспечивает доступ к координатам точек и их первым производным по параметру **_t_**, что позволяет использовать эти объекты в различных математических и графических задачах.

## 3. Использование

### Проект включает в себя следующие файлы:

* **curve.h** - содержит объявления классов _Curve_, _Circle_, _Ellips_, и _Helix_, а также структуры _Point_.
* **curve.cpp** - содержит реализации методов классов.
* **generate_curves.h** и **generate_curves.cpp** - содержат функции для генерации случайных объектов и их коллекций.
* **main.cpp** - демонстрирует пример использования классов для создания случайных объектов, вывода их координат и производных, а также сортировки их по радиусу в случае кругов.

## 4.Описание методов

### Класс Curve

* **std::optional<Point> GetPointAtT _(double t)_** - возвращает точку на кривой для заданного параметра t. Возвращает std::nullopt, если t находится вне допустимого диапазона.
* **std::optional<Point> GetFirstDerivativeAtT _(double t)_** - возвращает первую производную точки на кривой по параметру t. Возвращает std::nullopt, если t находится вне допустимого диапазона.

  ### Класс Circle _(наследник от Curve)_

  * **Circle _(const Point& center, double radius)_** - конструктор класса _Circle_. Принимает центр круга и его радиус.
  * **const double GetRadius _()_** - возвращает радиус круга.

  ### Класс Ellips _(наследник от Curve)_

  * **Ellips _(const Point& center, double radius_x, double radius_y)_** - конструктор класса _Ellips_. Принимает центр эллипса и его полуоси.
  * **const std::pair<double, double> GetRadii _()_**: - возвращает пару, представляющую полуоси эллипса.

  ### Класс Helix _(наследник от Curve)_

  * **Helix _(const Point& center, double radius, double step)_** - конструктор класса _Helix_. Принимает центр спирали, её радиус и шаг.
  * **const double GetRadius _()_** - возвращает радиус спирали.

## План развития

### Планы развития проекта включают в себя:

* Расширение функциональности библиотеки для работы с другими типами геометрических объектов.
* Оптимизация методов вычисления координат и производных для улучшения производительности.
* Добавление примеров использования и дополнительной документации для упрощения внедрения библиотеки в проекты.
