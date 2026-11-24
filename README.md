# -Power-Shell-
Код в Power Shell, который переносит добавленные языковые пакеты из раздела Token(Speech_OneCore) в Token (Speech)
Код изменяет: 
1.Название на аналогичные как в Speech например было: MSTTS_V110_enUS_DavidM -> TTS_MS_EN-US_David_11.0
2.Первые два параметра на аналогичные. Например Microsoft David - English (United States) -> Microsoft David Desktop- English (United States)
3. Путь параметра LangDataPath и VoicePath удаляя из пути значения параметра _OneCore. Например: %windir%\Speech_OneCore\Engines\TTS\en-US\M1033David -> %windir%\Speech\Engines\TTS\en-US\M1033David
4. Код изменять/удалять из раздела Attributes:
4.1. Добавляет параметр SpLexicon и его значение брать у любого другого языкового пакета у которого такой параметр и его значение уже есть
4.2. Изменяет параметр Name, добавляя к нему Desktop. Например Microsoft David -> Microsoft David Desktop
4.3. Удаляет параметр DataVersion и SayAsSupport
