# Установка

Для правильной работы приложения, требуется установить дополнительные программы, которые автор благоразумно собрал и поместил все в один архиив.

1. Скачайте файл ```All_In_One_w64.zip``` со страницы автора проекта по адресу: https://github.com/romanvht/ByeDPIManager/releases/latest
    <details><summary>Картиночка</summary>

    ![](images/bdm_download_01.png)
    </details></br>

2. Найдите на своем компьютере скачанный файл.
    Нажмите правой клавишей на файле и выберите “Извлечь все…”
    <details><summary>Картиночка</summary>

    ![](images/bdm_install_01.png)
    </details></br>

3. В появившемся окне укажите, куда установите программу, в данном примере программа будет установлена в папку ```С:\APPS\ByeDPIManager```
    <details><summary>Картиночки</summary>

    ![](images/bdm_install_02.png)    </br>
    Такой состав папок и файлов должен быть после распаковки
    
    ![](images/bdm_install_03.png)</br></br>
    </details></br>

4. Далее перейдите в папку ```redist``` и установите оба приложения из нее. Данные программы нужны для корректной работы компонента ProxiFyre. 
- ```VC_redist.x64.exe``` ([Microsoft Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170#latest-microsoft-visual-c-redistributable-version))
    <details><summary>Картиночка</summary>

    ![](images/bdm_install_04.png)
    </details></br>
- ```Windows.Packet.Filter.3.6.1.1.x64.msi``` ([Windows Packet Filter](https://github.com/wiresock/ndisapi/releases/latest))
    <details><summary>Картиночка</summary>

    ![](images/bdm_install_05.png)
    </details></br>
Если Вы не доверяете файлам в архиве, то в скобках приведены ссылки на страницы скачивания данных программ с официиальных сайтов.

   >[!IMPORTANT]
   >**Если не были установлены данные программы, то невозможна корректная работа встроенного инструмента ProxiFyre и соответственно всего ByeDPI Manager**

5. На этом установка завершена и **обязательно** требуется [настройка](setting.md).