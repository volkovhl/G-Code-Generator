<p align="center">
  <a href="https://volkovhl.github.io/G-Code-Generator/">
    <img src="https://github.com/volkovhl/G-Code-Generator/raw/main/G-code-Generator.webp" alt="G-code Generator Preview" width="640" style="border-radius:12px; box-shadow: 0 8px 32px rgba(0,0,0,0.5);">
  </a>
</p>

<h1 align="center">
  ⚙️ G-code Generator
</h1>

<p align="center">
  <strong>Генератор G-кода для CNC 3018 (GRBL) с поддержкой лазера и спиральной заливки</strong><br>
  Контур • Рамка • Спираль • Лазерный режим
</p>

<p align="center">
  <a href="https://volkovhl.github.io/G-Code-Generator/">
    <img src="https://img.shields.io/badge/ЗАПУСТИТЬ_ДЕМО-00D4FF?style=for-the-badge&logo=google-chrome&logoColor=white&labelColor=111" alt="Live Demo">
  </a>
  &nbsp;
  <a href="https://github.com/volkovhl/G-Code-Generator/stargazers">
    <img src="https://img.shields.io/github/stars/volkovhl/G-Code-Generator?style=for-the-badge&logo=github&logoColor=white&labelColor=111" alt="Stars">
  </a>
  &nbsp;
  <a href="https://github.com/volkovhl/G-Code-Generator/blob/main/LICENSE">
    <img src="https://img.shields.io/github/license/volkovhl/G-Code-Generator?style=for-the-badge&logo=opensourceinitiative&logoColor=white&labelColor=111" alt="License">
  </a>
</p>

<p align="center">
  <img src="https://github.com/volkovhl/G-Code-Generator/raw/main/preview-example.webp" alt="Пример генерации G-code" width="520" style="border-radius:16px; box-shadow: 0 8px 32px rgba(0,0,0,0.5);">
</p>

---

## ✨ Возможности

<div align="center">

  <table>
    <tr>
      <td align="center" width="130">▢ ◯ ⬡<br><b>Квадрат / Прямоугольник<br>Круг / Шестигранник</b></td>
      <td align="center" width="130">📐 🖼️<br><b>Контур • Рамка</b></td>
      <td align="center" width="130">🌀<br><b>Спираль (заливка)</b></td>
      <td align="center" width="130">🔥 🔧<br><b>Лазер • Сверление</b></td>
    </tr>
  </table>

</div>

- **Точная траектория** с учётом диаметра фрезы (компенсация радиуса)
- **Сторона контура** — внешний (столбик) или внутренний (вырез)
- **Скругления углов** (отдельные внешний / внутренний радиусы для рамки)
- **Рамка** — внешний контур смещён наружу, внутренний внутрь и развёрнут; подъём Z между контурами
- **Спиральная заливка** — от центра к краю с припуском и чистовым проходом
- **Лазерный режим** (M3/M5 + мощность S, без перемещений по Z)
- **Центровое сверление** перед заливкой (для спирали)
- **Шаг (stepover)**, снятие за проход по Z, припуск на чистовую
- **Удобный предпросмотр** траектории в реальном времени (можно отключить)
- **Полностью адаптивный** интерфейс (удобно на телефоне)

---

## 🛠 Технологии

- **Чистый стек**: HTML + CSS + JavaScript (без внешних зависимостей)
- **Генерация G-code** на лету
- **Canvas** для интерактивного предпросмотра траектории
- **GRBL / Candle / LaserGRBL / UGS** — полная совместимость

---

## 📲 Как использовать

1. Откройте **[демо](https://volkovhl.github.io/G-Code-Generator/)**
2. Выберите форму, режим и параметры
3. Нажмите **«Сгенерировать»**
4. Скопируйте G-code или скачайте `.nc` файл
5. Отправьте в Candle / LaserGRBL / Universal G-code Sender

> 💡 **Советы**:
> - Для лазера включайте «Лазерный режим» — код будет без перемещений по Z, с M3/M5.
> - В режиме «Контур» выбирайте сторону: внешний (материал остаётся внутри) или внутренний (вырез).
> - В режиме «Рамка» внешний контур смещается наружу, внутренний — внутрь и разворачивается для правильного направления фрезерования.
> - Для тяжёлых спиралей можно отключить визуализацию — G-code всё равно генерируется.

---

## 🎯 Режимы работы

| Режим | Описание |
|-------|----------|
| **Контур** | Внешний или внутренний контур. Внешний — материал остаётся внутри (столбик). Внутренний — материал остаётся снаружи (вырез/отверстие). |
| **Рамка** | Внешний контур (смещён **наружу**) + внутренний (смещён **внутрь** и **развёрнут**), с подъёмом Z между ними. Отдельные радиусы скругления и толщина стенки. |
| **Спираль (заливка)** | Заполняет всю площадь от центра к краю. Черновая спираль с припуском + чистовой контур для точного размера. |

---

## 🔧 Параметры фрезеровки

- **Диаметр фрезы** — траектория автоматически смещается на радиус
- **Глубина за проход** и **количество проходов**
- **Подача (F)**
- **Шаг (stepover)** — перекрытие проходов в % от диаметра фрезы
- **Снятие за проход (по Z)** — для спиральной заливки
- **Припуск на чистовую (stock to leave)** — остаток для точного чистового прохода
- **Центровое сверление** — перед началом спиральной заливки

---

## 🔥 Лазерный режим

- Генерация без команд по Z
- M5 при подъезде и между контурами
- M3 Sxxx только во время реза
- Поддержка спиральной заливки
- Мощность S настраивается (обычно 0–1000 для LaserGRBL)

---

<p align="center">
  <a href="https://volkovhl.github.io/G-Code-Generator/">▶️ Запустить генератор</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/volkovhl/G-Code-Generator">📂 Исходный код</a>
</p>

<p align="center">
  <sub>MIT License • Сделано с ❤️ в Russia</sub>
</p>
