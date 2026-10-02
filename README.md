# Mantella RU Piper

Русские голоса [Piper](https://github.com/OHF-Voice/piper1-gpl) для [Mantella](https://www.nexusmods.com/skyrimspecialedition/mods/98631) (Skyrim SE/AE): 22 модели (medium), дообученные на оригинальной русской озвучке Skyrim, включая DLC. Они заменяют английские модели Piper в Mantella для тех же типов голосов.

**Скачать:** архив `Mantella-RU-Piper-1.0.zip` в [Releases](../../releases), 1,2 ГБ.

## Голоса
- **Женские (10):** femalecommander, femalecommoner, femalecondescending, femaledarkelf, femaleelfhaughty, femaleeventoned, femalenord, femaleorc, femalesultry, femaleyoungeager.
- **Мужские (12):** maleargonian, malebrute, malecommoner, malecommoneraccented, malecondescending, maleelfhaughty, maleeventoned, maleeventonedaccented, malekhajiit, malenord, maleorc, maleyoungeager.

## Установка (MO2)
1. Установи архив как обычный мод.
2. Поставь его ниже Mantella и ниже «Mantella - Expanded Piper Models List», если он есть.
3. В `config.ini` Mantella выставь `tts_service = Piper`. Меняй, когда Mantella закрыта.

Модели лежат в `SKSE/Plugins/MantellaSoftware/piper/models/skyrim/low/<тип голоса>.onnx` (+ `.onnx.json`). Из конфигов `.onnx.json` убраны многосимвольные фонемы, иначе `piper.exe` из Mantella их не читает.

## Ограничения
- В мужских голосах слышны «роботизированные» искажения.
- Ударения иногда ставятся неверно: так фонемизирует espeak-ng.

## Как сделано
Голоса дообучены в piper1-gpl на Google Colab и Kaggle. Базовые модели взяты из [rhasspy/piper-voices](https://huggingface.co/rhasspy/piper-voices):
- женские голоса — от `ru_RU-irina-medium` (датасет RHVoice; в карточке модели лицензия указана как Unknown);
- maleelfhaughty и maleeventoned — от `ru_RU-ruslan-medium` (датасет [RUSLAN](https://ruslan-corpus.github.io/), CC BY-NC-SA 4.0);
- остальные мужские — от `ru_RU-dmitri-medium` (датасет OHF-Voice/voice-datasets, CC0).

## Лицензия и права
- Мод некоммерческий и бесплатный. Модели на базе ruslan распространяются на условиях [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/).
- Голоса — производные от озвучки The Elder Scrolls V: Skyrim (Bethesda Softworks) и работы русских актёров озвучания. Все права на оригинальную озвучку принадлежат их владельцам. Если вы правообладатель или актёр озвучания и против публикации, откройте issue — мод будет убран.
