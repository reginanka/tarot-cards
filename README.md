# 🔮 Tarot Cards WebP Collection

Full 78-card Tarot deck + card back in **WebP** format.  
Ready to use via CDN — no need to host the files yourself.

Повна колода Таро (78 карт + рубашка) у форматі **WebP**.  
Зручно підключати через CDN без завантаження файлів.

**Repository:** [https://github.com/reginanka/tarot-cards](https://github.com/reginanka/tarot-cards)  
**CDN base:** `https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/`

---

## 📐 Specifications / Специфікації

| Parameter / Параметр | Value / Значення |
|----------------------|------------------|
| Format               | WebP |
| Dimensions           | 848 × 1264 px |
| Cards                | 78 + card back |
| Deck style           | Classic 78-card Tarot (Justice VIII, Strength XI) |
| License              | [CC BY 4.0](LICENSE.md) |

---

## 🏷️ Naming Scheme / Схема найменування

### Major Arcana (`m00` – `m21`)
- `m00` → The Fool / Дурень  
- `m01` → The Magician / Маг  
- …  
- `m21` → The World / Світ  

### Minor Arcana
| Prefix | Suit (EN)   | Suit (UA)  | Range       |
|--------|-------------|------------|-------------|
| `w`    | Wands       | Жезли      | `w01`–`w14` |
| `c`    | Cups        | Кубки      | `c01`–`c14` |
| `s`    | Swords      | Мечі       | `s01`–`s14` |
| `p`    | Pentacles   | Пентаклі   | `p01`–`p14` |

**Rank numbers / Номери рангів:**

| #  | EN     | UA        | #  | EN     | UA        |
|----|--------|-----------|----|--------|-----------|
| 01 | Ace    | Туз       | 08 | Eight  | Вісімка   |
| 02 | Two    | Двійка    | 09 | Nine   | Дев'ятка  |
| 03 | Three  | Трійка    | 10 | Ten    | Десятка   |
| 04 | Four   | Четвірка  | 11 | Page   | Паж       |
| 05 | Five   | П'ятірка  | 12 | Knight | Лицар     |
| 06 | Six    | Шістка    | 13 | Queen  | Королева  |
| 07 | Seven  | Сімка     | 14 | King   | Король    |

**Card back / Рубашка:** `card-back.webp`

---

## 🚀 Quick Start (CDN)

### HTML
```html
<img
  src="https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m00.webp"
  alt="The Fool"
  width="212"
  height="316"
/>
```

### JavaScript
```js
const CDN = 'https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/';

function cardUrl(filename) {
  return CDN + filename;
}

console.log(cardUrl('m00.webp'));      // The Fool / Дурень
console.log(cardUrl('w01.webp'));      // Ace of Wands / Туз Жезлів
console.log(cardUrl('card-back.webp'));
```

### Example card array / Приклад масиву карт
```js
const CDN = 'https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/';

const majorArcana = [
  { id: 'm00', name: 'The Fool',     name_ua: 'Дурень', image: CDN + 'm00.webp' },
  { id: 'm01', name: 'The Magician', name_ua: 'Маг',    image: CDN + 'm01.webp' },
  // ... see full list in the tables below
];
```

---

## 📦 Ready-to-use JSON with descriptions / Готовий JSON з описами

We also provide a complete **`cards.json`** file — perfect for developers.

Також підготували повний **`cards.json`** — зручний файл для розробників з усіма 78 картами.

Each card object contains:
- `id` and `filename`
- English and Ukrainian names (`name` / `name_ua`)
- Arcana type (`arcana`: `major` / `minor`)
- Number
- **Full upright & reversed meanings** (`upright` / `upright_en`, `reversed` / `reversed_en`)
- Element (`element`)

Кожна карта містить:
- `id` та `filename`
- назви англійською та українською (`name` / `name_ua`)
- тип аркану (`arcana`: major / minor)
- номер
- **повні описи** прямої та перевернутої позиції (`upright` / `upright_en`, `reversed` / `reversed_en`)
- елемент (`element`)

**CDN / Direct link:**
```
https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards.json
```

or

```
https://raw.githubusercontent.com/reginanka/tarot-cards/main/cards.json
```

### Usage example / Приклад використання

```js
const response = await fetch('https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards.json');
const cards = await response.json();

// Find a card by id
const fool = cards.find(c => c.id === 'm00');
console.log(fool.name_ua);        // Дурень
console.log(fool.upright);        // український опис
console.log(fool.upright_en);     // English description
```

Just fetch the JSON and you get both high-quality images (via CDN) and rich bilingual interpretations — ready for any frontend project.

Просто завантажуєш JSON і маєш і картинки (через CDN), і якісні двомовні тлумачення — готово для будь-якого фронтенд-проєкту.

---

## 📋 Full Card List / Повний список карт

### Major Arcana / Старші Аркани

| Card (EN)          | Card (UA)       | Filename   | CDN URL |
|--------------------|-----------------|------------|---------|
| The Fool           | Дурень          | `m00.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m00.webp) |
| The Magician       | Маг             | `m01.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m01.webp) |
| The High Priestess | Жриця           | `m02.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m02.webp) |
| The Empress        | Імператриця     | `m03.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m03.webp) |
| The Emperor        | Імператор        | `m04.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m04.webp) |
| The Hierophant     | Ієрофант        | `m05.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m05.webp) |
| The Lovers         | Закохані        | `m06.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m06.webp) |
| The Chariot        | Колісниця       | `m07.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m07.webp) |
| Justice            | Справедливість  | `m08.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m08.webp) |
| The Hermit         | Відлюдник       | `m09.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m09.webp) |
| Wheel of Fortune   | Колесо Фортуни  | `m10.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m10.webp) |
| Strength           | Сила            | `m11.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m11.webp) |
| The Hanged Man     | Повішений       | `m12.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m12.webp) |
| Death              | Смерть          | `m13.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m13.webp) |
| Temperance         | Помірність      | `m14.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m14.webp) |
| The Devil          | Диявол          | `m15.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m15.webp) |
| The Tower          | Вежа            | `m16.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m16.webp) |
| The Star           | Зірка           | `m17.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m17.webp) |
| The Moon           | Місяць          | `m18.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m18.webp) |
| The Sun            | Сонце           | `m19.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m19.webp) |
| Judgement          | Суд             | `m20.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m20.webp) |
| The World          | Світ            | `m21.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/m21.webp) |

### Wands / Жезли

| Card (EN)       | Card (UA)        | Filename   | CDN URL |
|-----------------|------------------|------------|---------|
| Ace of Wands    | Туз Жезлів       | `w01.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w01.webp) |
| Two of Wands    | Двійка Жезлів    | `w02.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w02.webp) |
| Three of Wands  | Трійка Жезлів    | `w03.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w03.webp) |
| Four of Wands   | Четвірка Жезлів  | `w04.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w04.webp) |
| Five of Wands   | П'ятірка Жезлів  | `w05.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w05.webp) |
| Six of Wands    | Шістка Жезлів    | `w06.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w06.webp) |
| Seven of Wands  | Сімка Жезлів     | `w07.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w07.webp) |
| Eight of Wands  | Вісімка Жезлів   | `w08.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w08.webp) |
| Nine of Wands   | Дев'ятка Жезлів  | `w09.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w09.webp) |
| Ten of Wands    | Десятка Жезлів   | `w10.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w10.webp) |
| Page of Wands   | Паж Жезлів       | `w11.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w11.webp) |
| Knight of Wands | Лицар Жезлів     | `w12.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w12.webp) |
| Queen of Wands  | Королева Жезлів  | `w13.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w13.webp) |
| King of Wands   | Король Жезлів    | `w14.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/w14.webp) |

### Cups / Кубки

| Card (EN)      | Card (UA)       | Filename   | CDN URL |
|----------------|-----------------|------------|---------|
| Ace of Cups    | Туз Кубків      | `c01.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c01.webp) |
| Two of Cups    | Двійка Кубків   | `c02.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c02.webp) |
| Three of Cups  | Трійка Кубків   | `c03.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c03.webp) |
| Four of Cups   | Четвірка Кубків | `c04.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c04.webp) |
| Five of Cups   | П'ятірка Кубків | `c05.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c05.webp) |
| Six of Cups    | Шістка Кубків   | `c06.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c06.webp) |
| Seven of Cups  | Сімка Кубків    | `c07.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c07.webp) |
| Eight of Cups  | Вісімка Кубків  | `c08.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c08.webp) |
| Nine of Cups   | Дев'ятка Кубків | `c09.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c09.webp) |
| Ten of Cups    | Десятка Кубків  | `c10.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c10.webp) |
| Page of Cups   | Паж Кубків      | `c11.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c11.webp) |
| Knight of Cups | Лицар Кубків    | `c12.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c12.webp) |
| Queen of Cups  | Королева Кубків | `c13.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c13.webp) |
| King of Cups   | Король Кубків   | `c14.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/c14.webp) |

### Swords / Мечі

| Card (EN)        | Card (UA)        | Filename   | CDN URL |
|------------------|------------------|------------|---------|
| Ace of Swords    | Туз Мечів        | `s01.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s01.webp) |
| Two of Swords    | Двійка Мечів     | `s02.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s02.webp) |
| Three of Swords  | Трійка Мечів     | `s03.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s03.webp) |
| Four of Swords   | Четвірка Мечів   | `s04.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s04.webp) |
| Five of Swords   | П'ятірка Мечів   | `s05.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s05.webp) |
| Six of Swords    | Шістка Мечів     | `s06.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s06.webp) |
| Seven of Swords  | Сімка Мечів      | `s07.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s07.webp) |
| Eight of Swords  | Вісімка Мечів    | `s08.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s08.webp) |
| Nine of Swords   | Дев'ятка Мечів   | `s09.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s09.webp) |
| Ten of Swords    | Десятка Мечів    | `s10.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s10.webp) |
| Page of Swords   | Паж Мечів        | `s11.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s11.webp) |
| Knight of Swords | Лицар Мечів      | `s12.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s12.webp) |
| Queen of Swords  | Королева Мечів   | `s13.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s13.webp) |
| King of Swords   | Король Мечів     | `s14.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/s14.webp) |

### Pentacles / Пентаклі

| Card (EN)           | Card (UA)            | Filename   | CDN URL |
|---------------------|----------------------|------------|---------|
| Ace of Pentacles    | Туз Пентаклів        | `p01.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p01.webp) |
| Two of Pentacles    | Двійка Пентаклів     | `p02.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p02.webp) |
| Three of Pentacles  | Трійка Пентаклів     | `p03.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p03.webp) |
| Four of Pentacles   | Четвірка Пентаклів   | `p04.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p04.webp) |
| Five of Pentacles   | П'ятірка Пентаклів   | `p05.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p05.webp) |
| Six of Pentacles    | Шістка Пентаклів     | `p06.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p06.webp) |
| Seven of Pentacles  | Сімка Пентаклів      | `p07.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p07.webp) |
| Eight of Pentacles  | Вісімка Пентаклів    | `p08.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p08.webp) |
| Nine of Pentacles   | Дев'ятка Пентаклів   | `p09.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p09.webp) |
| Ten of Pentacles    | Десятка Пентаклів    | `p10.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p10.webp) |
| Page of Pentacles   | Паж Пентаклів        | `p11.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p11.webp) |
| Knight of Pentacles | Лицар Пентаклів      | `p12.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p12.webp) |
| Queen of Pentacles  | Королева Пентаклів   | `p13.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p13.webp) |
| King of Pentacles   | Король Пентаклів     | `p14.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/p14.webp) |

### Card Back / Рубашка

| Description | Filename         | CDN URL |
|-------------|------------------|---------|
| Card back   | `card-back.webp` | [link](https://cdn.jsdelivr.net/gh/reginanka/tarot-cards@main/cards/card-back.webp) |

---

## 📜 License & Attribution / Ліцензія та атрибуція

This collection is released under the **[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE.md)** license.

Ця колекція поширюється під ліцензією **[Creative Commons Attribution 4.0 International (CC BY 4.0)](LICENSE.md)**.

**Required attribution / Обов’язкове посилання:**

> Tarot Cards WebP Collection by Gearberry — [https://github.com/reginanka/tarot-cards](https://github.com/reginanka/tarot-cards)

---

## 👤 Developer & Socials

Developed ❤️ by **Gearberry**.  
Feel free to connect with me:

- [Telegram](https://t.me/Gearberry)
- [YouTube](https://www.youtube.com/@Gearberry)
- [Instagram](https://www.instagram.com/gearberry_)
- [Facebook](https://www.facebook.com/profile.php?id=61586878866628)
- [Threads](https://www.threads.com/@gearberry_)


[![Rehina Nanaka profile views](https://u8views.com/api/v1/github/profiles/212413806/views/day-week-month-total-count.svg)](https://u8views.com/github/reginanka)
