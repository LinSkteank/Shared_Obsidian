VS Code поддерживает расширение фрагмента Emmet . Сокращения Emmet перечислены вместе с другими предложениями и фрагментами в списке автозаполнения редактора.

![[emmetsnippet.gif]]

> **Совет:** см. раздел HTML в [шпаргалке Emmet](https://docs.emmet.io/cheat-sheet/) , где указаны допустимые сокращения.

Если вы хотите использовать сокращения HTML Emmet с другими языками, вы можете связать один из режимов Emmet (например `css`, , `html`) с другими языками с помощью `emmet.includeLanguages` [параметра](https://code-visualstudio-com.translate.goog/docs/getstarted/settings?_x_tr_sl=en&_x_tr_tl=ru&_x_tr_hl=ru&_x_tr_pto=wapp) . Параметр принимает [идентификатор языка](https://code-visualstudio-com.translate.goog/docs/languages/overview?_x_tr_sl=en&_x_tr_tl=ru&_x_tr_hl=ru&_x_tr_pto=wapp#_language-identifier) и связывает его с идентификатором языка режима, поддерживаемого Emmet.

Например, чтобы использовать HTML-аббревиатуры Emmet внутри JavaScript:
```html
{
 "emmet.includeLanguages": {
 "javascript": "html"
 }
}
```