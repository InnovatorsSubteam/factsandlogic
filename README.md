# Современные плюсцы))
## Фичи новых стандартов
### Фичи языка
#### Ослабленные требования к `constexpr` позволящие писать более сложный код. Одна из его фишек это более строгая проверка и запрет на UB в теле функции. Константы полеезнее так же делать как `constexpr`, а не дефайнами ибо у компилятора будет  информация о типах и он сможет предупредить о неожиданных переполнениях, например
#### Больше трейтов в стандартной библиотеки позволяющих вместо своих непроверенных костылей использовать стандартные провереннные средства и оставлять код более читаемым
#### `constexpr` шаблонные переменный позвоялющие вместо `typename std::enable_if<std::is_same<T1, T2>::value, U>::type` просто `std::enable_if_t<std::is_same_v<T1, T2>, U>` что опять же увеличивает читаемость кода, освобождая его от служебных нагромождений
#### Структурное связывание, позволяющее давать осмысленный имена при пробеге по мапам, вместо пары с ничего не говорящих .first и .second
#### `constexpr if` облегачющий написание шаблонных функция со SFINAE делающий их более читабельными вместо копипасты общих участков функции в две почти идентичные(пример в simple_job.h)

#### Чем полезно их наличие / вредно отсутствие
### Фичи стандартной библиотеки
#### Чем полезно их наличие / вредно отсутствие
#### Чем можно заменить при использовании старых стандартов языка
## Фичи современных компиляторов
### Чем мешает отсутствие возможности компилировать ими на проде
