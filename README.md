# monodevelop-settings
У этого проекта две основные цели. Во-первых, упрощение внедрения стиля кодирования. Во-вторых, сохранение и распространение лучших практик использования MonoDevelop.
## Что внутри?
 * Настройки для автоматического форматирования кода. 
 * Настройки именования.
 * Настройки хоткеев. 
 * Code templates(ctor) адаптированные под наш стиль кодирования.

## Как установить настройки?
Настройки устанавливаются простым клонированием репозитория в нужную папку.
```bash
mkdir ~/Library/MonoDevelop-3.0-orig/
cp -R ~/Library/MonoDevelop-3.0/ ~/Library/MonoDevelop-3.0-orig/
rm -rf ~/Library/MonoDevelop-3.0/
git clone https://github.com/gaech/monodevelop-settings.git ~/Library/MonoDevelop-3.0/
```
## Пользователям Windows
Пользователи Windows клонируют репозиторий в любое удобное место на компьютере, и далее ручками копируют папки Policies и Snippets в папку
```bash
C:\Users\%USERNAME%\AppData\Roaming\MonoDevelop-X.X
```
Копировать папку KeyBindings, равно как и делать репозиторий напрямую в папке настроек монодевелопа не рекомендуется. У макоси нет клавиши Control, а у винды нет клавиши Meta, так что их хоткеи несовместимы.

После успешного клонирования надо изменить глобальные настройки MonoDevelop. `MonoDevelop → Preferences...`
В разделе `Source code → .NET Naming Policies` выставляем `Policy: Touchin`

![](https://github.com/gaech/monodevelop-settings/raw/014f6c45b1b40f69aeba8641a3cca22af635abd9/Screenshots/global-naming-policies.jpg) 

В разделе `Source code → Code Formatting → C# source code` выставляем `Policy: Touchin`

![](https://github.com/gaech/monodevelop-settings/raw/2622dd2c61fe2cb0cbf9cd8220285ac95ab7c199/Screenshots/global-code-formating.jpg)

В разделе `Source code → Name Conventions` выставляем `Policy: Touchin`  (для Monodeveop 2.8 и младше, походу, неактуально)

![](https://github.com/gaech/monodevelop-settings/raw/014f6c45b1b40f69aeba8641a3cca22af635abd9/Screenshots/global-name-convention.jpg)

Для того чтобы MonoDevelop выделял места, где нарушается соглашение о кодировании, можно включить анализ кода `Other → Source Analysis`

![](https://github.com/gaech/monodevelop-settings/raw/b2c2185b757fb934668d73ae1a79c9ad76448059/Screenshots/source-analysis.jpg) 

Настройки будут влиять на новые проекты и решения. В существующих надо изменить настройки вручную. 

Если по какой-то причине вы не хотите использовать все общие настройки, то можно скопировать отдельно нужны вам файлы. 

## Обновление настроек
```bash
cd ~/Library/MonoDevelop-3.0/
git pull origin master
```

Пользователи Windows делают почти то же самое, но в другую папку, и потом ручками заново копируют нужные настройки в AppData.

## Как поделиться своими наработками?
 * Сделать fork проекта. Для этого достаточно нажать кнопку Fork на этой странице.
 * Склонировать форк.
 * Закоммитить свои изменения.
 * Отправить изменения в основной репозиторий. Это делается с помощью кнопки Pull request.

## Ссылки 
 * https://github.com/gaech/coding-style

## TODO
 * Подсказка по хоткеям MonoDevelop
 * Подсказка по шаблонам кода