---
title: PayPath — политика конфиденциальности
description: PayPath не собирает данные. Всё остаётся на устройстве.
---

# Политика конфиденциальности PayPath

**Приложение:** PayPath (`com.paypath.paypath`)
**Разработчик:** Олег Алексеев
**Связь:** oleg@moraltogether.com
**Дата вступления в силу:** 10 сентября 2026

## Коротко

PayPath не собирает никаких данных о вас. У приложения нет аккаунтов, нет сервера и нет синхронизации. Всё, что вы вводите — кредиты, суммы, даты, номера договоров, фотографии — остаётся в памяти вашего устройства и никуда не передаётся.

## Какие данные вы вводите и где они хранятся

Приложение хранит на устройстве:

- сведения о кредитах: название, банк, номер договора, суммы, сроки, ставки, графики платежей и историю их изменений;
- фотографии договоров, если вы их добавляете, — в личном каталоге приложения;
- настройки: язык, валюту, напоминания, категории;
- если вы включили блокировку приложения — **хэш** PIN-кода со случайной солью в защищённом хранилище платформы (Android Keystore). Сам PIN не хранится ни в каком виде.

Всё перечисленное лежит в приватном хранилище приложения. Другие приложения к нему доступа не имеют. Автоматическое резервное копирование Android для приложения отключено (`allowBackup="false"`), поэтому эти данные не уезжают и в облако Google.

## Что уходит в сеть

Один запрос, и только он: приложение обращается к **публичному API Банка Израиля** (`edge.boi.gov.il`), чтобы узнать текущую ставку Банка Израиля и рассчитать по ней Прайм.

- Запрос содержит только код статистической серии и диапазон дат. **Никаких ваших данных в нём нет** — ни сумм, ни договоров, ни идентификаторов устройства.
- Запрос выполняется без авторизации, ответ публичный: те же цифры Банк Израиля показывает на своём сайте всем.
- Обращение можно **полностью отключить** переключателем «Авто-обновление Прайма» в настройках. При выключенном переключателе сетевой путь не используется вовсе, а ставку можно вводить вручную.

Других сетевых обращений в приложении нет. В нём нет аналитики, нет счётчиков посещаемости, нет систем сбора отчётов о сбоях и нет рекламы.

## Резервные копии, которые делаете вы

В настройках есть «Сохранить на устройство» и «Поделиться копией». Это ваше действие и ваш выбор: копия создаётся только когда вы нажимаете кнопку, и уходит туда, куда вы её отправите — в выбранную папку на устройстве или в приложение, которое вы выберете в системном меню «Поделиться».

**Важно:** такая копия содержит все ваши данные, включая суммы и номера договоров. Дальнейшая её судьба зависит от того, куда вы её передали, и политикой этого приложения уже не регулируется. Приложение никогда не отправляет копии само.

## Разрешения и зачем они

| Разрешение | Зачем |
|---|---|
| Интернет | только запрос ставки Банка Израиля, см. выше |
| Камера | сфотографировать договор и приложить к кредиту |
| Уведомления, вибрация | напоминания о предстоящих платежах |
| Запуск после перезагрузки | чтобы уже назначенные напоминания не потерялись после перезагрузки телефона |
| Биометрия, отпечаток | разблокировка приложения, если вы включили блокировку |

Биометрию проверяет сама операционная система. Приложение получает только ответ «да» или «нет» и не имеет доступа ни к отпечатку, ни к другим биометрическим данным.

## Чем PayPath не является

PayPath — калькулятор и личный учёт: он считает по тем данным, которые вы ввели руками. Приложение **не оказывает финансовых услуг**. Оно не выдаёт кредиты, не переводит деньги, не подключается к банковским счетам и не является платёжным сервисом. Расчёты носят справочный характер; при расхождении с выпиской и графиком банка верны документы банка.

## Дети

Приложение предназначено для учёта личных кредитов и не адресовано детям. Никаких данных, включая данные детей, оно не собирает.

## Ваши права

Все данные находятся у вас на устройстве и полностью в вашем распоряжении. Любой кредит можно удалить в приложении. Чтобы удалить всё сразу, достаточно удалить приложение — вместе с ним удаляется и его хранилище. Запрашивать удаление данных у разработчика не требуется: у разработчика их нет.

## Изменения

Если политика изменится, здесь появится новая дата вступления в силу. Существенные изменения будут отражены в описании обновления приложения.

## Вопросы

oleg@moraltogether.com

---

# PayPath Privacy Policy

**App:** PayPath (`com.paypath.paypath`)
**Developer:** Oleg Alexeyev
**Contact:** oleg@moraltogether.com
**Effective date:** 10 September 2026

## In short

PayPath collects no data about you. There are no accounts, no server and no synchronisation. Everything you enter — loans, amounts, dates, contract numbers, photographs — stays in your device's storage and is never transmitted anywhere.

## What you enter and where it is kept

The app stores on your device:

- loan details: name, bank, contract number, amounts, terms, rates, payment schedules and the history of their changes;
- photographs of contracts, if you add them, in the app's private directory;
- settings: language, currency, reminders, categories;
- if you enable the app lock, a salted **hash** of your PIN in the platform's secure storage (Android Keystore). The PIN itself is never stored in any form.

All of this lives in the app's private storage, which other apps cannot reach. Android's automatic backup is disabled for the app (`allowBackup="false"`), so this data does not reach Google's cloud either.

## What leaves the device

One request, and only this one: the app calls the **Bank of Israel public API** (`edge.boi.gov.il`) to read the current Bank of Israel rate and derive the Prime rate from it.

- The request carries only a statistical series code and a date range. **None of your data is in it** — no amounts, no contracts, no device identifiers.
- It is unauthenticated and the response is public: the Bank of Israel shows the same figures to everyone on its website.
- It can be **switched off entirely** with the "Prime auto-update" toggle in settings. With the toggle off the network path is not used at all, and the rate can be entered by hand.

The app makes no other network requests. It contains no analytics, no usage tracking, no crash reporting and no advertising.

## Backups you make yourself

Settings offers "Save to device" and "Share a copy". This is your action and your choice: a copy is created only when you press the button, and goes wherever you send it — a folder you pick on the device, or an app you pick from the system share sheet.

**Note:** such a copy contains all of your data, including amounts and contract numbers. What happens to it afterwards depends on where you sent it and is no longer governed by this policy. The app never sends copies on its own.

## Permissions and why

| Permission | Why |
|---|---|
| Internet | only the Bank of Israel rate request described above |
| Camera | photograph a contract and attach it to a loan |
| Notifications, vibration | reminders about upcoming payments |
| Receive boot completed | so that already scheduled reminders survive a phone restart |
| Biometrics, fingerprint | unlocking the app, if you enabled the app lock |

Biometrics are verified by the operating system itself. The app receives only a yes-or-no answer and has no access to your fingerprint or any other biometric data.

## What PayPath is not

PayPath is a calculator and a personal ledger: it computes from the data you enter by hand. The app **provides no financial services**. It does not lend money, transfer funds, connect to bank accounts, or act as a payment service. Its figures are informational; where they differ from your bank's statement and schedule, the bank's documents are correct.

## Children

The app is for tracking personal loans and is not directed at children. It collects no data at all, including data about children.

## Your rights

All data is on your device and entirely under your control. Any loan can be deleted in the app. To remove everything at once, uninstall the app — its storage is removed with it. There is no need to request deletion from the developer: the developer does not have your data.

## Changes

If this policy changes, a new effective date will appear here. Material changes will be noted in the app's release notes.

## Questions

oleg@moraltogether.com
