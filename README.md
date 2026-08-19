<div align="center">

# MARSIAGO

**Разработчик плагинов Minecraft**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Paper](https://img.shields.io/badge/Paper-0288D1?style=flat-square)
![Spigot](https://img.shields.io/badge/Spigot-F5A623?style=flat-square)
![Bukkit API](https://img.shields.io/badge/Bukkit%20API-62B47A?style=flat-square)
![Telegram](https://img.shields.io/badge/@marsiago-26A5E4?style=flat-square&logo=telegram&logoColor=white)

Держу и администрирую собственный PvP-сервер, для него же пишу механики.<br>
Восемь плагинов работают в проде — около 12 000 строк.<br>
Это не учебные проекты: они крутятся на живых людях и чинятся, когда ломаются.

</div>

---

## Плагины здесь

<table>
<tr>
<td width="33%" valign="top">

### [WantedPosters](https://github.com/marsiago/wanted-posters)

Плакаты розыска: печать по команде, стена топа на спавне, картинка в Discord, объявления в чат.

**Внутри:** отрисовка карт через `java.awt`, скины при `online-mode=false`, multipart-webhook

</td>
<td width="33%" valign="top">

### [WantedCases](https://github.com/marsiago/wanted-cases)

Объявляет в чат, что кому-то выпало из кейса.

**Внутри:** у источника нет ни события, ни API — ловится перехватом пакета `SYSTEM_CHAT`

</td>
<td width="33%" valign="top">

### [WantedCrowd](https://github.com/marsiago/wanted-crowd)

Награды растут от числа активных игроков онлайн.

**Внутри:** платит за совпадение по времени, а не за вход; отсечка AFK

</td>
</tr>
</table>

---

## Что умею

**Плагины** — Paper/Spigot, Bukkit API. Всё отгруженное сейчас работает на
1.21.x под Java 21; под другую версию ядра собирается так же, с поправкой на
изменения API. Сборка без Gradle и Maven, напрямую через `javac`, когда так
быстрее и не нужна сеть.

**Интеграция с закрытыми плагинами** — когда у соседа нет ни API, ни событий,
нужный метод ищется по jar-у через `javap` и вызывается рефлексией, а события
ловятся перехватом пакетов ProtocolLib.

**Мягкие зависимости** — классы, ссылающиеся на чужой плагин, вынесены отдельно
и грузятся только после проверки, что он есть; иначе `NoClassDefFoundError`
роняет всё. Изоляция проверяется отдельным ClassLoader'ом, а не на глаз.

**Графика и тексты** — динамическая отрисовка карт, ресурспаки, кастомные шрифты
и глифы, озвучка с расчётом пауз по реальной длине `.ogg`.

**Наружу** — вебхуки Discord и Telegram, PlaceholderAPI, Vault, LuckPerms,
WorldGuard, TAB.

**Администрирование** — настройка и оптимизация Paper, античит, права, регионы,
авторизация, разбор логов и статистики сервера скриптами.

---

## Работаю на заказ

Плагины с нуля · доработка и починка чужих, в том числе без исходников ·
настройка сервера под ключ · разбор лагов и падений

Отдаю jar, исходники, README с устройством плагина и `config.yml`, в котором
прокомментирован каждый ключ — включая то, почему число именно такое.

| Услуга | От |
|---|---|
| Плагин с нуля по ТЗ | 3 000 ₽ |
| Доработка или починка существующего | 1 500 ₽ |
| Настройка сервера под ключ | 4 000 ₽ |
| Разбор лагов, падений, низкого TPS | 2 000 ₽ |

<div align="center">

### [Написать в Telegram → @marsiago](https://t.me/marsiago)

<br>

<img src="assets/cat.jpg" width="340" alt="Кот на клавиатуре">

*код-ревью проходит строго*

</div>
