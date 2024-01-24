# README

[#id-8-bitnyi-kompyuter-svoimi-lapkami](./#id-8-bitnyi-kompyuter-svoimi-lapkami "mention")

[#registry](./#registry "mention")

[#nabor-komand](./#nabor-komand "mention")

##

## 8 битный компьютер своими лапками

Основная цель данного проекта разработать архетиктуру и собрать простой 8 битный компьютер не используя сложных чипов и микропроцессоров. Такой вариант ограничений позволяет лучше разобраться в устройстве компьютеров и продемонстрировать насколько сложны казалось бы повседневные вещи. Ниже предствален дорожная карта проекта и документация.

* [ ] Изучение литературы
* [ ] Обазначение архитектуры
* [ ] Разработка схемотехники
* [ ] Симуляция схемотехники
* [ ] Сборка прототипа на макетной плате
* [ ] Разработка схемы печатной плате
* [ ] Сборка окончательного продукта на печатной плате
* [ ] Тестирование и демонстарция продукта



## Регистры

Архетиктура имеет 8 регистров(кодируются 3 битами).

<table><thead><tr><th width="79">Регистр</th><th width="294">Назначение</th></tr></thead><tbody><tr><td>RA</td><td>Арифметические и логические операции</td></tr><tr><td>RB</td><td>Арифметические и логические операции</td></tr><tr><td>RC</td><td>Арифметические и логические операции</td></tr><tr><td>RJ</td><td>Условные переходы</td></tr><tr><td>RL</td><td>Указатель</td></tr><tr><td>RS</td><td>Регистр стека</td></tr><tr><td>RX</td><td>Регистр свободного пользования</td></tr><tr><td>RY</td><td>Регистр свободного пользования</td></tr></tbody></table>

## Набор команд

Инструкция представляет собой 8 битное слово.

<table><thead><tr><th width="252">Мнемоника</th><th width="251">Операция</th><th width="207">Операнды</th></tr></thead><tbody><tr><td>NOOP</td><td>-</td><td>-</td></tr><tr><td>NAND</td><td>RC ← RA NAND RB</td><td>-</td></tr><tr><td>NOR</td><td>RC ← RA NOR RB</td><td>-</td></tr><tr><td>SHR</td><td>биитовый сдвиг вправо RC ← RA </td><td>-</td></tr><tr><td>ROR</td><td>циклический битовый сдвиг вправо RC ← RA</td><td>-</td></tr><tr><td>ADD</td><td>RC ← RA + RB</td><td>-</td></tr><tr><td>SUB</td><td>RC ← RA -RB</td><td>-</td></tr><tr><td>INC</td><td>RC + 1</td><td>-</td></tr><tr><td>DEC</td><td>RC -1</td><td>-</td></tr><tr><td>JMPL</td><td>если RL &#x3C; 0, CL ← RL</td><td>-</td></tr><tr><td>JMPM</td><td>если RL > 0, CL ← RL</td><td>-</td></tr><tr><td>JMPE</td><td>если RL = 0, CL ← RL</td><td>-</td></tr><tr><td>JMPC</td><td>если Carry = 1, CL ← RL</td><td></td></tr><tr><td>JUMP</td><td>безусловный переход</td><td>-</td></tr><tr><td>MOV</td><td>reg2 ← reg1</td><td>reg1, reg2</td></tr><tr><td>READ</td><td>RC ← mem[RL]</td><td>-</td></tr><tr><td>WRT</td><td>mem[RL] ← RC</td><td>-</td></tr><tr><td>IN</td><td>RC ← PORTIN</td><td>reg</td></tr><tr><td>OUT</td><td>PORTOUT ← reg</td><td>reg</td></tr></tbody></table>
