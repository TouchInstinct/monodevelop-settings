# monodevelop-settings
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
После успешного клонирования надо изменить глобальные настройки MonoDevelop. `MonoDevelop → Preferences...`
В разделе `Source code → .NET Naming Policies` выставляем `Policy: Touchin`
![](https://github.com/gaech/monodevelop-settings/raw/014f6c45b1b40f69aeba8641a3cca22af635abd9/Screenshots/global-naming-policies.jpg) 

В разделе `Source code → Code Formatting → C# source code` выставляем `Policy: Touchin`
![](https://github.com/gaech/monodevelop-settings/raw/2622dd2c61fe2cb0cbf9cd8220285ac95ab7c199/Screenshots/global-code-formating.jpg)

В разделе `Source code → Name Conventions` выставляем `Policy: Touchin`
![](https://github.com/gaech/monodevelop-settings/raw/014f6c45b1b40f69aeba8641a3cca22af635abd9/Screenshots/global-name-convention.jpg)

Настройки будут влиять на новые проекты и решения. В существующих надо изменить настройки вручную. 

Если по какой-то причине вы не хотите использовать все общие настройки, то можно скопировать отдельно нужны вам файлы. 

## Обновление настроек
```bash
cd ~/Library/MonoDevelop-3.0/
git pull origin master
```