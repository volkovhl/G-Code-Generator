<p align="center">
  <a href="https://volkovhl.github.io/G-Code-Generator/">
    <img src="https://github.com/volkovhl/G-Code-Generator/raw/main/G-code-Generator.webp" alt="G-code Generator Preview" width="640" style="border-radius:12px; box-shadow: 0 8px 32px rgba(0,0,0,0.5);">
  </a>
</p>

<h1 align="center">
  ⚙️ G-code Generator
</h1>

<p align="center">
  <strong>Генератор G-кода для CNC 3018 (GRBL) с поддержкой лазера и сверления</strong><br>
  Контур • Рамка • Окно • Лазерный режим
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
      <td align="center" width="120">▢<br><b>Квадрат / Прямоугольник / Круг</b></td>
      <td align="center" width="120">📐<br><b>Контур • Рамка • Окно</b></td>
      <td align="center" width="120">🔥<br><b>Лазерный режим</b></td>
      <td align="center" width="120">🔧<br><b>Сверление</b></td>
    </tr>
  </table>
</div>

- **Точная траектория** с учётом диаметра фрезы (компенсация радиуса)
- **Скругления углов** (отдельные внешний/внутренний радиусы для рамки)
- **Лазерный режим** (M3/M5 + мощность S, без Z)
- **Режим сверления** с периодическим подъёмом фрезы для выхода стружки
- **Подъём Z** между внешним и внутренним контуром рамки
- **Удобный предпросмотр** траектории в реальном времени
- **Полностью адаптивный** интерфейс (удобно на телефоне)

---

## 🛠 Технологии

- **Чистый стек**: HTML + CSS + JavaScript (без внешних зависимостей)
- **Генерация G-code** на лету
- **Canvas** для интерактивного предпросмотра
- **GRBL / Candle / LaserGRBL** — полная совместимость

---

## 📲 Как использовать

1. Откройте **[демо](https://volkovhl.github.io/G-Code-Generator/)**
2. Выберите форму, режим и параметры
3. Нажмите **«Сгенерировать»**
4. Скопируйте G-code или скачайте `.nc` файл
5. Отправьте в Candle / LaserGRBL / UGS

> 💡 **Совет**: Для лазера включайте «Лазерный режим» — код будет без перемещений по Z.

---

## 🎯 Режимы работы

- **Контур** — внешний контур (материал остаётся внутри)
- **Рамка** — внешний + внутренний контур с подъёмом Z между ними
- **Окно** — вырезание отверстия + опциональное сверление по центру

---

<p align="center">
  <a href="https://volkovhl.github.io/G-Code-Generator/">▶️ Запустить генератор</a>
  &nbsp;•&nbsp;
  <a href="https://github.com/volkovhl/G-Code-Generator">📂 Исходный код</a>
</p>

<p align="center">
  <sub>MIT License • Сделано с ❤️ в Russia</sub>
</p>
