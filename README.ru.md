[![Версия](https://img.shields.io/github/release/greymass/eos-voter/all.svg)](https://github.com/greymass/eos-voter/releases)
[![Проблемы](https://img.shields.io/github/issues/greymass/eos-voter.svg)](https://github.com/greymass/eos-voter/issues)
[![Лицензия](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/greymass/eos-voter/master/LICENSE)
[![Загрузки](https://img.shields.io/github/downloads/greymass/eos-voter/total.svg)

[English](https://github.com/greymass/eos-voter/blob/master/README.md) - [한글](https://github.com/greymass/eos-voter/blob/master/README.kr.md) - [中文](https://github.com/greymass/eos-voter/blob/master/README.zh.md) - [日本語](https://github.com/greymass/eos-voter/blob/master/README.ja.md) - [Русский](https://github.com/greymass/eos-voter/blob/master/README.ru.md)

# eos-voter - Голосование за Производителей Блоков и кошелёк

`eos-voter` - это ограниченный функциональный выпуск лёгкого кошелька, предназначенного для блокцепи EOS. Это приложение может использоваться для подключения к удалённой конечной точке API EOS для голосования за производителей блоков и выполнения основных команд кошелька.


[![eos-voter screenshot](https://raw.githubusercontent.com/greymass/eos-voter/master/eos-voter.png)](https://raw.githubusercontent.com/greymass/eos-voter/master/eos-voter.png)

### Особенности

- ** Голосование за Производителей Блоков **: выбрать и проголосовать за производителей блоков. Обратите внимание, что пользовательский интерфейс для голосования за производителей блоков не является инструментом исследования; это простой интерфейс, обеспечивающий безопасный способ голосования.
- ** Передачи Токенов **: Передача EOS или любых другой токенов которые есть на вашем балансе.
- ** Резервация процессорных мощностей и пропускной способности сети **: Закрепление токенов EOS для резервации ресурсов сети. Закреплённые токены предоставляют права на использование ресурсов сети, и учитываются при голосовании за производителей блоков.
- ** Локальный кошелек **: установите пароль при импорте личного ключа, чтобы создать локальный кошелёк. Этот ключ будет зашифрован локально, используя этот пароль. Этот пароль потребуется каждый раз, когда вам нужно разблокировать кошелек.
- ** Временное использование **: если вы предпочитаете не хранить ваши ключи в приложении, просто выберите не устанавливать пароль. Когда приложение закроется, ваш ключ будет забыт.

## Получить eos-voter

### Релизы

Текущая версия 0.7.1:

- [Windows Installer](https://github.com/greymass/eos-voter/releases/download/v0.7.1/win-eos-voter-0.7.1.exe)
- [macOS Package](https://github.com/greymass/eos-voter/releases/download/v0.7.1/mac-eos-voter-0.7.1.dmg)
- [Linux (deb)](https://github.com/greymass/eos-voter/releases/download/v0.7.1/linux-eos-voter-0.7.1-amd64.deb)
- [Linux (snap)](https://github.com/greymass/eos-voter/releases/download/v0.7.1/linux-eos-voter-0.7.1-amd64.snap)

Последняя версия всегда будет доступна на странице выпусков этого репозитория:

[https://github.com/greymass/eos-voter/releases](https://github.com/greymass/eos-voter/releases)

Чтобы определить, какой файл вам нужен, если вы ...

- ** Пользователь MacOS **: Загрузите файл DMG (`eos-voter - ***. Dmg`) или ZIP (` eos-voter - *** - mac.zip`).
- ** Пользователь Windows **: Загрузите файл EXE (eos-voter - ***. Exe).
- ** Пользователь Linux **: Загрузите файл SNAP (`eos-voter - *** -_ amd64.snap`) или DEB (` eos-voter - *** -_ amd64.deb`)

### Безопасность: закрытые ключи

При использовании `eos-voter` все транзакции подписываются внутри приложения, и ваш ключ никуда не передается. Если указан пароль локального кошелька, приложение также сохранит и зашифрует ваш ключ для дальнейшего использования, используя шифрование AES-256. Текущая схема шифрования пароля / ключа [в настоящее время находится здесь] (https://github.com/aaroncox/eos-voter/blob/master/app/shared/actions/wallet.js#L71-L86).

### Конечные точки

Мы предлагаем публичный список узлов в этом репозитории для использования с этим приложением:

[Https://github.com/greymass/eos-voter/blob/master/nodes.md](https://github.com/greymass/eos-voter/blob/master/nodes.md)

Этот список будет обновляться с течением времени и на него можно ссылаться из окна начального подключения в приложении.

### Самостоятельная сборка

Если вы хотите собрать приложение самостоятельно, убедитесь, что у вас есть nodejs / npm / yarn, уже установленные локально.

** Примечание **: Если вы собираете это приложение в среде разработки Windows, потребуются дополнительные действия.

```
git clone https://github.com/greymass/eos-voter.git eos-voter
cd eos-voter
npm install
cd app
npm install
cd ..
```

Затем либо:

- MacOS: `npm run package-mac`
- Linux: `npm run package-linux`
- Windows: `npm run package-win`

Созданные файлы будут расположены в папке `releases` в корневой папке проекта.

### Запуск режима разработки

```
git clone https://github.com/greymass/eos-voter.git eos-voter
cd eos-voter
npm install
npm run dev
```

### Кредиты

Разработка этого приложения ведется членами команды [Greymass] (https://greymass.com), с тем чтобы заинтересованные стороны могли участвовать в управлении EOS.

### Подписи Выпусков

Чтобы проверить целостность выпусков, загружаемых с GitHub, ниже приведены результаты shasum для каждого из двоичных файлов:

Signed by [jesta on keybase](https://keybase.io/jesta)

```
-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA512

shasum -b -a 512 linux-eos-voter-0.7.1-amd64.deb
15861e901a0165256c6c5465f00a50c86f098d0d62b54b6e71d681cea61fb9c3f1823acc534761f330d0b63592af2a900c5f541301e6fe52a407219bffde6e4f *linux-eos-voter-0.7.1-amd64.deb
shasum -b -a 512 linux-eos-voter-0.7.1-arm64.deb
180aacf9a3d14149e845be2c757b08ac4aabebe20146e0795afb57b996f16da53cd147c5780e3569b67190b7daf9b5d28070c039f89220ab17178d6cbe7123f1 *linux-eos-voter-0.7.1-arm64.deb
shasum -b -a 512 linux-eos-voter-0.7.1-armv7l.deb
98eca71ffec54a25482ff761735bb459c7c86937922080c3cb3da211b22f21a3ede3bfc5cdbbc3c311c57a5e4e42d2a7fa47dc63a95e4f66022a9b78484fdb92 *linux-eos-voter-0.7.1-armv7l.deb
shasum -b -a 512 linux-eos-voter-0.7.1-x86_64.AppImage
95a869d47d0f9da9fc6c38a865023b8f390e9b2dd0b845196ad07d2d393f97b3cc2aeee84e837fe5a8114a5bc48b580768dc0d2a00b6f6773c04290660f0e939 *linux-eos-voter-0.7.1-x86_64.AppImage
shasum -b -a 512 mac-eos-voter-0.7.1.dmg
4a15a343d1c48e967ef885ed132698adce416648138ab02a697d97c15ea242d652280d0c7d9605ff0c8da62a9878dac6b2b11cd61b04e26642a6560c42c83017 *mac-eos-voter-0.7.1.dmg
shasum -b -a 512 mac-eos-voter-0.7.1.zip
fc39b8bc81300010f724f492def4b662fa4b19a53835eb54ae794d87e5243b8b29e8419617809744e537c3cd350e71e978e27c9bf6afc6a56739f6169b68cbe2 *mac-eos-voter-0.7.1.zip
shasum -b -a 512 win-eos-voter-0.7.1.exe
a51861b9c346c8b27f7d1ff30b19713bcb1e03e839c013c76bf4e2c16d4c0ef96f377a848f0fb896f5f34b9ceee4ca3f5011628b2880a8a6f0e29a2e609edc45 *win-eos-voter-0.7.1.exe
-----BEGIN PGP SIGNATURE-----
Version: Keybase OpenPGP v2.0.80
Comment: https://keybase.io/crypto

wsFcBAABCgAGBQJcPRQqAAoJECyLxnO05hN939EP/jApAWSxQ4uU8itZYzp7AcoZ
47Rxy/PSexOX+xYSzI88yiKBtbja8nL4zeDMg20mHNzg/oPTpci6BGqrHC8EP6kj
NC6L5/JZ8fO+27J+6/gsjYyFboRFjeklj1lHCjAtZkDp5oRLQNamUoNgWEV63eDM
8UfERE1Lax+tqPCkSxqXY5QENY+SgKox19JYSoBkR7pDC35du9Dn7t/CTQnYItwa
4c2pC5WLI+17WPfUmhn7kopcp7vmpSqy7gCgiHEAa2k3rOwuE9UXoM+EXiNNNNx+
vY0k4+r8KVmnhKlWxHVAysS0UYRe0bo7WcveIhT8nJ0ltyFZsdwboWDdnxJm85Rd
cdlOIxpHY+awXYQEM/sX21nhAckg3v6KDsfkDJlIzjYuAL5qjxrEZ1OsRtROjCA3
Lksy63RAcuzVeJQYg6RrDcHfx2X/JzNEbon1yp1n7DYt5FljC7qfYz4rgi/Jfjbb
/W04y4zt4rZ2e1qd1CARYfc3A/mkK4iiUf5xbR3p5HuY00mm335FLSo/JAoAyODf
OtyORVfRhkA/VZtSSDfbkFFa+lycs57eUoHXu9QReVxTZPQ0j++o1PT4CFx0Jote
TUkHxD8y9+z/QBra5iTnqozv83bGh3+HK3RFysRv0EE9Q1blQg2PZ04Q4JFBTi46
MsudY7AswJPMk7QFO4LM
=UzbA
-----END PGP SIGNATURE-----
```
