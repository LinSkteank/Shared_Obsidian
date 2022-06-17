---
type: paper
tags: 📥️/📜️/🩳/💻/🕸
aliases:
  - 
cssclass: 
---



# Title: **[[тэг optgroup в select 2021-10-13]]]**
- `Type:` [[&]]
- `Links:`
- `Reviewed Date:` [[2021-10-13]]



Иногда требуется разбить список на отдельные группы, не связанные между собой. Для этих целей был введен тег `<optgroup>`.
Чтобы озаглавить группу, используется атрибут `label`.


```html
<select>  
	<optgroup label = "Лето">  
		<option value = "s6">Июнь</option>  
		<option value = "s7">Июль</option>  
		<option value = "s8">Август</option>  
	</optgroup>  
	<optgroup label = "Зима">  
	<option value = "s12">Декабрь</option>  
	<option value = "s1">Январь</option>  
	<option value = "s2">Февраль</option>  
	</optgroup>  
</select>
```

<select>  
	<optgroup label = "Лето">  
		<option value = "s6">Июнь</option>  
		<option value = "s7">Июль</option>  
		<option value = "s8">Август</option>  
	</optgroup>  
	<optgroup label = "Зима">  
	<option value = "s12">Декабрь</option>  
	<option value = "s1">Январь</option>  
	<option value = "s2">Февраль</option>  
	</optgroup>  
</select>