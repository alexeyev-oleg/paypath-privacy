---
title: PayPath — политика конфиденциальности
description: PayPath не собирает данные. Всё остаётся на устройстве.
---

# Политика конфиденциальности PayPath

**Приложение:** PayPath (`com.paypath.paypath`)
**Разработчик:** CrazyDuck
**Связь:** support.crazyduck@gmail.com
**Дата вступления в силу:** 23 сентября 2026

## Коротко

У PayPath нет своего сервера и нет учётных записей у разработчика. Всё, что вы вводите — кредиты, суммы, даты, номера договоров, фотографии, — хранится в памяти вашего устройства.

Есть одно исключение, и вы включаете его сами: **семейная копия в вашем собственном Google Drive**. Пока вы её не включили, из приложения не уходит ничего, кроме запроса ставки Банка Израиля. Если включили — в ваш Drive уезжает копия ваших данных, **зашифрованная на телефоне** вашим паролем. Ни Google, ни разработчик прочитать её не могут: пароль не покидает ваше устройство.

Данные разработчику не передаются никогда — ни в каком виде и ни при каких настройках.

## Какие данные вы вводите и где они хранятся

Приложение хранит на устройстве:

- сведения о кредитах: название, банк, номер договора, суммы, сроки, ставки, графики платежей и историю их изменений;
- фотографии договоров, если вы их добавляете, — в личном каталоге приложения;
- настройки: язык, валюту, напоминания, категории;
- если вы включили блокировку приложения — **хэш** PIN-кода со случайной солью в защищённом хранилище платформы (Android Keystore). Сам PIN не хранится ни в каком виде.

Всё перечисленное лежит в приватном хранилище приложения. Другие приложения к нему доступа не имеют. Автоматическое резервное копирование Android для приложения отключено (`allowBackup="false"`), поэтому эти данные не уезжают и в облако Google.

## Что уходит в сеть

### Ставка Банка Израиля

Приложение обращается к **публичному API Банка Израиля** (`edge.boi.gov.il`), чтобы узнать текущую ставку и рассчитать по ней Прайм.

- Запрос содержит только код статистической серии и диапазон дат. **Никаких ваших данных в нём нет** — ни сумм, ни договоров, ни идентификаторов устройства.
- Запрос выполняется без авторизации, ответ публичный: те же цифры Банк Израиля показывает на своём сайте всем.
- Обращение можно **полностью отключить** переключателем «Авто-обновление Прайма» в настройках. При выключенном переключателе сетевой путь не используется вовсе, а ставку можно вводить вручную.

### Семейная копия в вашем Google Drive — только если вы её подключили

Это необязательная возможность, выключенная по умолчанию. Она нужна, когда кредиты ведут два человека в семье и обоим нужно видеть общую картину.

**Что происходит, когда вы её подключаете:**

- вы входите в **свой** аккаунт Google прямо в приложении и задаёте пароль на копию;
- приложение собирает архив с вашими данными — кредитами, суммами, датами, номерами договоров и фотографиями, — **шифрует его на телефоне** вашим паролем и кладёт в папку PayPath в вашем Google Drive;
- рядом с текущей копией раз в неделю откладывается датированный слепок; слепки живут около месяца и нужны на случай, если телефон потерян;
- вы можете открыть доступ к своей копии **одному человеку** по его адресу Google и закрыть его в любой момент — список тех, кому открыто, приложение показывает в настройках;
- вы можете указать копию, которую открыл вам другой человек; тогда его кредиты появятся у вас **только для просмотра**, а ваши записи останутся вашими.

**Кто что видит.** Google хранит файл, но прочитать его не может: файл зашифрован до того, как покинул телефон, а пароль хранится только в защищённом хранилище вашего устройства и никуда не отправляется. Разработчик не видит ни файла, ни пароля, ни самого факта, что вы чем-то пользуетесь: серверов у приложения нет. Человек, которому вы открыли доступ, видит содержимое копии — для этого он должен знать тот же пароль, и сообщаете его вы сами, вне приложения.

**Какие права в Google запрашиваются.** Только доступ к файлам, которые создало само приложение, и к файлу, который вы явно выбрали в окне Google. Остальное содержимое вашего Drive приложению недоступно.

**Обмен без нажатия кнопки.** Если семейная копия подключена, приложение обменивается с Drive само — **не чаще трёх раз в сутки** и только при открытии приложения. Когда ни у вас, ни у второго телефона ничего не изменилось, в сеть уходит один короткий служебный запрос, а сама копия не пересылается. Этот автоматический обмен выключается переключателем «Обновлять при открытии»; тогда копия уходит и приходит только по вашей кнопке.

### Больше ничего

Других сетевых обращений в приложении нет. В нём нет аналитики, нет счётчиков посещаемости, нет систем сбора отчётов о сбоях и нет рекламы.

## Резервные копии, которые делаете вы

В настройках есть «Сохранить на устройство» и «Поделиться копией». Это ваше действие и ваш выбор: копия создаётся только когда вы нажимаете кнопку, и уходит туда, куда вы её отправите — в выбранную папку на устройстве или в приложение, которое вы выберете в системном меню «Поделиться».

**Важно:** такая копия содержит все ваши данные, включая суммы и номера договоров. Дальнейшая её судьба зависит от того, куда вы её передали, и политикой этого приложения уже не регулируется. Кроме семейной копии в вашем Google Drive, описанной выше, приложение никуда ничего не отправляет само.

## Разрешения и зачем они

| Разрешение | Зачем |
|---|---|
| Интернет | запрос ставки Банка Израиля; если вы подключили семейную копию — обмен с вашим Google Drive |
| Аккаунт Google | только если вы подключаете семейную копию: вход в ваш аккаунт и доступ к файлам, созданным приложением |
| Камера | сфотографировать договор и приложить к кредиту |
| Уведомления, вибрация | напоминания о предстоящих платежах |
| Запуск после перезагрузки | чтобы уже назначенные напоминания не потерялись после перезагрузки телефона |
| Биометрия, отпечаток | разблокировка приложения, если вы включили блокировку |

Биометрию проверяет сама операционная система. Приложение получает только ответ «да» или «нет» и не имеет доступа ни к отпечатку, ни к другим биометрическим данным.

## Чем PayPath не является

PayPath — калькулятор и личный учёт: он считает по тем данным, которые вы ввели руками. Приложение **не оказывает финансовых услуг**. Оно не выдаёт кредиты, не переводит деньги, не подключается к банковским счетам и не является платёжным сервисом. Расчёты носят справочный характер; при расхождении с выпиской и графиком банка верны документы банка.

## Дети

Приложение предназначено для учёта личных кредитов и не адресовано детям. Никаких данных, включая данные детей, оно не собирает.

## Ваши права и как всё удалить

Все данные находятся у вас на устройстве и полностью в вашем распоряжении. Любой кредит можно удалить в приложении.

**Данные на телефоне.** Чтобы удалить всё сразу, удалите приложение — вместе с ним удаляется и его хранилище.

**Данные в облаке.** В настройках, в разделе Google Drive, есть кнопка **«Удалить копию и отключить»**. Она убирает из вашего Drive копию этого телефона и все недельные слепки, стирает пароль и все облачные настройки и отключает аккаунт Google с отзывом выданного доступа. Копии, которые открыли вам другие люди, остаются у них — приложение просто перестаёт о них знать.

Если в момент удаления телефон не в сети или доступ к Google уже отозван, приложение об этом скажет: местные следы оно уберёт, но файл в облаке останется. Тогда удалите его вручную в Google Диске, в папке **PayPath**.

**Учётной записи у разработчика у вас нет** — регистрация в приложении не предусмотрена, и запрашивать удаление данных у разработчика не требуется: у него их нет.

## Изменения

Если политика изменится, здесь появится новая дата вступления в силу. Существенные изменения будут отражены в описании обновления приложения.

## Вопросы

support.crazyduck@gmail.com

---

# PayPath Privacy Policy

**App:** PayPath (`com.paypath.paypath`)
**Developer:** CrazyDuck
**Contact:** support.crazyduck@gmail.com
**Effective date:** 23 September 2026

## In short

PayPath has no server of its own and the developer holds no accounts. Everything you enter — loans, amounts, dates, contract numbers, photographs — is kept in your device's storage.

There is one exception, and you switch it on yourself: **a family copy in your own Google Drive**. Until you turn it on, nothing leaves the app except the Bank of Israel rate request. Once you do, a copy of your data goes to your Drive **encrypted on the phone** with your password. Neither Google nor the developer can read it: the password never leaves your device.

Data is never sent to the developer — in any form and under any setting.

## What you enter and where it is kept

The app stores on your device:

- loan details: name, bank, contract number, amounts, terms, rates, payment schedules and the history of their changes;
- photographs of contracts, if you add them, in the app's private directory;
- settings: language, currency, reminders, categories;
- if you enable the app lock, a salted **hash** of your PIN in the platform's secure storage (Android Keystore). The PIN itself is never stored in any form.

All of this lives in the app's private storage, which other apps cannot reach. Android's automatic backup is disabled for the app (`allowBackup="false"`), so this data does not reach Google's cloud either.

## What leaves the device

### The Bank of Israel rate

The app calls the **Bank of Israel public API** (`edge.boi.gov.il`) to read the current rate and derive the Prime rate from it.

- The request carries only a statistical series code and a date range. **None of your data is in it** — no amounts, no contracts, no device identifiers.
- It is unauthenticated and the response is public: the Bank of Israel shows the same figures to everyone on its website.
- It can be **switched off entirely** with the "Prime auto-update" toggle in settings. With the toggle off the network path is not used at all, and the rate can be entered by hand.

### A family copy in your Google Drive — only if you connect it

This is optional and off by default. It exists for families where two people run the loans and both need the whole picture.

**What happens when you connect it:**

- you sign in to **your own** Google account inside the app and set a password for the copy;
- the app packs an archive of your data — loans, amounts, dates, contract numbers and photographs — **encrypts it on the phone** with your password, and puts it in a PayPath folder in your Google Drive;
- alongside the current copy, a dated snapshot is kept once a week; snapshots live about a month and exist in case the phone is lost;
- you can open your copy to **one person** by their Google address and close it again at any time; the app shows in settings who it is open to;
- you can point the app at a copy someone else opened to you; their loans then appear on your phone **for viewing only**, and your own records stay yours.

**Who sees what.** Google stores the file but cannot read it: it is encrypted before it leaves the phone, and the password is kept only in your device's secure storage and is never transmitted. The developer sees neither the file, nor the password, nor even the fact that you use the feature: the app has no servers. The person you opened the copy to can read its contents — for that they must know the same password, which you tell them yourself, outside the app.

**What is requested from Google.** Access only to files the app itself created, plus the one file you explicitly pick in Google's own chooser. The rest of your Drive is out of the app's reach.

**Exchange without pressing a button.** When the family copy is connected, the app exchanges data with Drive on its own — **at most three times a day**, and only when you open the app. If nothing has changed on your phone or on the other one, a single short service request goes out and the copy itself is not transferred. This automatic exchange is switched off with the "Update when the app opens" toggle; the copy then goes out and comes in only when you press the button.

### Nothing else

The app makes no other network requests. It contains no analytics, no usage tracking, no crash reporting and no advertising.

## Backups you make yourself

Settings offers "Save to device" and "Share a copy". This is your action and your choice: a copy is created only when you press the button, and goes wherever you send it — a folder you pick on the device, or an app you pick from the system share sheet.

**Note:** such a copy contains all of your data, including amounts and contract numbers. What happens to it afterwards depends on where you sent it and is no longer governed by this policy. Apart from the family copy in your own Google Drive described above, the app sends nothing anywhere on its own.

## Permissions and why

| Permission | Why |
|---|---|
| Internet | the Bank of Israel rate request; and, if you connected the family copy, the exchange with your Google Drive |
| Google account | only if you connect the family copy: signing in to your account and access to files the app created |
| Camera | photograph a contract and attach it to a loan |
| Notifications, vibration | reminders about upcoming payments |
| Receive boot completed | so that already scheduled reminders survive a phone restart |
| Biometrics, fingerprint | unlocking the app, if you enabled the app lock |

Biometrics are verified by the operating system itself. The app receives only a yes-or-no answer and has no access to your fingerprint or any other biometric data.

## What PayPath is not

PayPath is a calculator and a personal ledger: it computes from the data you enter by hand. The app **provides no financial services**. It does not lend money, transfer funds, connect to bank accounts, or act as a payment service. Its figures are informational; where they differ from your bank's statement and schedule, the bank's documents are correct.

## Children

The app is for tracking personal loans and is not directed at children. It collects no data at all, including data about children.

## Your rights and how to delete everything

All data is on your device and entirely under your control. Any loan can be deleted in the app.

**Data on the phone.** To remove everything at once, uninstall the app — its storage goes with it.

**Data in the cloud.** Settings, in the Google Drive section, has a **"Delete the copy and disconnect"** button. It removes this phone's copy and every weekly snapshot from your Drive, erases the password and all cloud settings, and disconnects the Google account with its access revoked. Copies other people opened to you stay with them — the app simply stops knowing about them.

If the phone is offline at that moment, or access to Google has already been revoked, the app says so: it clears the local traces, but the file in the cloud remains. Delete it by hand in Google Drive, in the **PayPath** folder.

**You have no account with the developer** — the app has no registration, and there is no need to request deletion from the developer: they do not have your data.

## Changes

If this policy changes, a new effective date will appear here. Material changes will be noted in the app's release notes.

## Questions

support.crazyduck@gmail.com
