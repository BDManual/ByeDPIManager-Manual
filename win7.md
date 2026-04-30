# Установка ByeDPI Manager на Windows 7

## Требования

* Windows 7 с пакетом обновлений SP1 или Windows Server 2008 R2 с пакетом обновлений SP1.
* .NET Framework 4.7.2–4.8 (рекомендуется) или .NET Runtime 9.

---

## Установка

1. Со страницы релизов [ByeDPI Manager](https://github.com/romanvht/ByeDPIManager/releases) в разделе **Assets** скачайте `All_in_one_w64.zip` и распакуйте его в подпапку проекта.

   > **Примечание.** Если у вас Windows 7 **64-bit**, пропустите шаги 2–3 и переходите к шагу 4.

2. *(Только для Windows 7 32-bit)* Со страницы релизов [proxifyre](https://github.com/wiresock/proxifyre/releases) в разделе **Assets** скачайте архив `ProxiFyre-...-x86-signed.zip`. Распакуйте содержимое архива в подпапку `libs\proxifyre` в каталоге ByeDPI Manager, заменив существующие файлы.

3. *(Только для Windows 7 32-bit)* Со страницы релизов [byedpi](https://github.com/hufrea/byedpi/releases) в разделе **Assets** скачайте архив `byedpi-...-i686-w64.zip`. Из архива распакуйте `ciadpi.exe` в подпапку `libs\byedpi` в каталоге ByeDPI Manager, заменив существующие файлы.

4. Убедитесь, что в системе установлен пакет обновлений SP1. Для проверки: нажмите `Win + Pause` или откройте «Мой компьютер» → ПКМ → «Свойства» — в открывшемся окне должно быть указано `Service Pack 1`.
   Если SP1 не установлен — установите SP1 и затем все доступные обновления Windows 7 через Центр обновлений; перезагрузите систему и продолжите установку с шага 5.

5. Установите обновление поддержки подписывания кода SHA-2 для Windows 7: [KB4474419](https://support.microsoft.com/ru-ru/topic/%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%BF%D0%BE%D0%B4%D0%B4%D0%B5%D1%80%D0%B6%D0%BA%D0%B8-%D0%BF%D0%BE%D0%B4%D0%BF%D0%B8%D1%81%D1%8B%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F-%D0%BA%D0%BE%D0%B4%D0%B0-sha-2-%D0%B4%D0%BB%D1%8F-windows-server-2008-r2-windows-7-%D0%B8-windows-server-2008-23-%D1%81%D0%B5%D0%BD%D1%82%D1%8F%D0%B1%D1%80%D1%8F-2019-%D0%B3-84a8aad5-d8d9-2d5c-6d78-34f9aa5f8339). Без этого обновления система может не распознавать подписи новых драйверов и исполняемых файлов.

6. Установите обновление стека обслуживания для Windows 7 SP1: [KB4490628](https://support.microsoft.com/ru-ru/topic/%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D1%81%D1%82%D0%B5%D0%BA%D0%B0-%D0%B4%D0%BB%D1%8F-windows-7-sp1-%D0%B8-windows-server-2008-r2-sp1-12-%D0%BC%D0%B0%D1%80%D1%82%D0%B0-2019-%D0%B3-b4dc0cff-d4f2-a408-0cb1-cb8e918feeba). Без этого обновления Центр обновлений может работать нестабильно (высокая нагрузка на `svchost.exe`, зависания при поиске/установке обновлений и т.п.).

7. Установите обновление универсальной среды выполнения C (Universal C Runtime): [KB2999226](https://support.microsoft.com/ru-ru/topic/%D0%BE%D0%B1%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B4%D0%BB%D1%8F-%D1%83%D0%BD%D0%B8%D0%B2%D0%B5%D1%80%D1%81%D0%B0%D0%BB%D1%8C%D0%BD%D0%BE%D0%B9-%D1%81%D1%80%D0%B5%D0%B4%D1%8B-%D0%B2%D1%8B%D0%BF%D0%BE%D0%BB%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F-c-%D0%B2-windows-c0514201-7fe6-95a3-b0a5-287930f3560c). Без этого пакета некоторые приложения (включая `proxifyre` и `curl.exe`) не будут запускаться и могут выдавать ошибки вида `System.IO.FileNotFoundException: ... socksify.dll`.

8. Установите MS Visual C++ Redistributable 2015–2022:

   * для 32-битных систем (x86): установите только
     [vc_redist.x86.exe](https://aka.ms/vs/17/release/vc_redist.x86.exe)

   * для 64-битных систем (x64): установите оба пакета
     [vc_redist.x86.exe](https://aka.ms/vs/17/release/vc_redist.x86.exe) и
     [vc_redist.x64.exe](https://aka.ms/vs/17/release/vc_redist.x64.exe)

9. Установите .NET:

   * Рекомендуется установить .NET Framework версии [4.7.2–4.8](https://support.microsoft.com/ru-ru/topic/microsoft-net-framework-4-8-%D0%B0%D0%B2%D1%82%D0%BE%D0%BD%D0%BE%D0%BC%D0%BD%D1%8B%D0%B9-%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D1%89%D0%B8%D0%BA-%D0%B4%D0%BB%D1%8F-windows-9d23f658-3b97-68ab-d013-aa3c3e7495e0).

   * Альтернативно, при необходимости можно установить .NET Runtime 9 (бинарные сборки доступны для [x86](https://dotnet.microsoft.com/ru-ru/download/dotnet/thank-you/runtime-9.0.9-windows-x86-binaries) и [x64](https://dotnet.microsoft.com/ru-ru/download/dotnet/thank-you/runtime-9.0.9-windows-x64-binaries)).

   > Примечание: .NET Framework 4.8.1 не поддерживается в Windows 7.

10. Со страницы релизов [Windows Packet Filter](https://github.com/wiresock/ndisapi/releases) в разделе **Assets** скачайте и установите подходящий пакет драйвера:

    * для 32-бит: `Windows.Packet.Filter...x86.msi`
    * для 64-бит: `Windows.Packet.Filter...x64.msi`

11. После выполнения всех описанных шагов продолжайте настройку и запуск ByeDPI Manager по оригинальной [инструкции](https://github.com/BDManual/ByeDPIManager-Manual/blob/main/setting.md).

---

## Примечания и рекомендации

* Пункты о KB4474419 (SHA-2), KB4490628 (стек обслуживания) и KB2999226 (UCRT) **обязательны** для корректной работы драйверов и сетевых компонентов. Даже если Центр обновлений формально работает, эти обновления могут отсутствовать на старых или частично обновлённых системах — проверьте их наличие в списке установленных обновлений.
* Если при установке драйвера или запуске `proxifyre` появляются ошибки, сначала проверьте установку указанных KB и наличие необходимых рантаймов (UCRT, Visual C++).
* Всегда создавайте точку восстановления системы или резервную копию важных данных перед установкой драйверов и системных обновлений.
