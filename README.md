# meteorsmap
Meteorites Visualisation Map

https://sw3nlab.github.io/meteorsmap

![image](https://raw.githubusercontent.com/sw3nlab/meteorsmap/main/arizona.gif)

### Онлайн 2D/3D карта для визуализации мест падения метеоритов (с 1492 до 1998 года) 

Данные + Координаты падения метеоритов взяты с Лаборатории Метеоритики Российской Академии Наук

( http://www.meteorites.ru/menu/collection/collect_a.html )


Для удобного и более наглядного анализа, составлена база данных на 688 метеоритов (файл dump.sql)


для визуализации используется SDK WorldWind от NASA ( docs/index.html подтягивает данные из файла coordinates.json )

( https://github.com/NASAWorldWind/WebWorldWind )




!!! описание большенства метеоритов отсутствует по причине отсутствия таковых сведений в Википедии 
(по каким метеоритам удалось найти инфу в википедии есть линк на статью, по остальным docs/404.html )

ниже представленна небольшая статистика по имеющимся данным...<br/>
```php
SQL>select count(id) from meteorites where type="Chondrite";
>432
SQL>select count(id) from meteorites where type="Iron";
>166
```
<br/>
![image](https://raw.githubusercontent.com/sw3nlab/meteorsmap/main/type.jpg)
<br/>
`SQL>select count(id) from meteorites where latitude>0;`
<br/>
![image](https://raw.githubusercontent.com/sw3nlab/meteorsmap/main/NS.png)
<br/>
```php
SQL>select count(id) from meteorites where latitude between 0 and 15;
>16
SQL>select count(id) from meteorites where latitude between 15 and 30;
>96
SQL>select count(id) from meteorites where latitude between 30 and 45;
>250
```
![image](https://raw.githubusercontent.com/sw3nlab/meteorsmap/main/total.png)
<br/>
