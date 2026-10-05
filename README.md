# MH-Miner

Демо-майнер Pearl (PRL) для NVIDIA. Публичный репозиторий содержит готовые
сборки и инструкции; исходники хранятся отдельно в приватном репозитории.

## Демо 0.1.0-demo1

- [Windows x64](https://github.com/MH-Miner-Official/MH-Miner-Releases/releases/download/v0.1.0-demo1/MH-Miner-0.1.0-demo1-windows-x64.zip)
- [Linux x64, Ubuntu 22.04](https://github.com/MH-Miner-Official/MH-Miner-Releases/releases/download/v0.1.0-demo1/MH-Miner-0.1.0-demo1-linux-x64.tar.gz)
- [Архив для HiveOS Custom Miner](https://github.com/MH-Miner-Official/MH-Miner-Releases/releases/download/v0.1.0-demo1/mhminer-0.1.0_demo1.tar.gz)
- [Готовый шаблон HiveOS для Kryptex](https://github.com/MH-Miner-Official/MH-Miner-Releases/releases/download/v0.1.0-demo1/HiveOS-Kryptex-MH-Miner.json)
- [SHA256SUMS](https://github.com/MH-Miner-Official/MH-Miner-Releases/releases/download/v0.1.0-demo1/SHA256SUMS)

Windows: распакуйте архив, откройте BAT выбранного пула и замените только
`YOUR_PRL_ADDRESS` на свой PRL-адрес. Доступны Kryptex, LuckyPool, HeroMiners,
Suprnova. По умолчанию используется одна GPU №0; остановка Ctrl+C.
Драйвер NVIDIA и Microsoft Visual C++ x64 runtime должны быть установлены.

HiveOS: Custom Miner `mhminer`, алгоритм `pearlhash`, установка по ссылке на
архив выше, шаблон кошелька `%WAL%.%WORKER_NAME%`. Для ручного пяти минутного
теста в распакованном каталоге: `bash start-hiveos.sh YOUR_PRL_ADDRESS mh-test 0`.

Комиссия разработчика: 1% как долгосрочная цель. На Kryptex первая developer-шара
идёт авансом после случайного сохранённого порога 10–20 принятых пользовательских
шар; затем аванс компенсируется более длинным пользовательским интервалом.
Учёт взвешен по сложности и сохраняется при обычном перезапуске. На других пулах
учёт основан на времени вычислений. На коротком тесте доля может быть выше 1%.

**Это экспериментальное демо.** Проверены RTX 3060 Ti, Windows и Linux через
WSL, 45 основных тестов, защищённые модули, локальные Stratum-сценарии и
авторизация четырёх пулов. Финальная Windows-сборка получила 3 принятые шары
на Kryptex. Actual HiveOS installation, RTX 4090/5090 and final developer-session
accepted/credit/payout remain to be verified. Полный статус: `VALIDATION.txt`
в архиве. Не выдавайте наличие старого баланса кошелька за подтверждение комиссии.

Скомпилированы native SM86/89/120. Несколько GPU одновременно в этом демо не
поддерживаются. Хешрейт локальный, без гарантии начисления или выплаты.
CUDA-модули зашифрованы в файлах; владелец компьютера может исследовать память.
Лицензии зависимостей сохранены в `LICENSES` каждого архива.
