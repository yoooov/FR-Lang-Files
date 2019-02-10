# U-232-V5

```
   _   _   _   _   _     _   _   _   _   _   _     _   _   _   _	
  / \ / \ / \ / \ / \   / \ / \ / \ / \ / \ / \   / \ / \ / \ / \	
 ( U | - | 2 | 3 | 2 )-( S | O | U | R | C | E )-( C | O | D | E )	
  \_/ \_/ \_/ \_/ \_/   \_/ \_/ \_/ \_/ \_/ \_/   \_/ \_/ \_/ \_/	

```

U-232 V5 -> High performance Bittorrent tracker

## French Language Pack

### Language Translator

- *yoooov*

##	Support Forum

- <http://u-232.servebeer.com/forum/index.php>

## Set Up Instructions:


Upload the files to your server to /lang/4

Then edit the following files of your U-232 V5 site:

### /usercp.php

After :
```bash
<option value='3'" . ($CURUSER['language'] == '3' ? " selected='selected'" : "") . ">New</option>
```

Add :
```bash
<option value='4'" . ($CURUSER['language'] == '4' ? " selected='selected'" : "") . ">FR</option>;
```

### /take_lang.php

After :
```bash
<option value='3'" . ($CURUSER['language'] == '3' ? " selected='selected'" : "") . ">Rm</option>
```

Add :
```bash
<option value='4'" . ($CURUSER['language'] == '4' ? " selected='selected'" : "") . ">FR</option>";
```

### /include/bittorrent.php

After :
```bash
case ($lang_charset == 3):
        return "ISO-8859-17";
```

Add :
```bash
case ($lang_charset == 4):
		return "UTF-8";
```

### and just check /include/config.php to verify the following is correct :
```bash
//==charset
$INSTALLER09['char_set'] = 'UTF-8'; //also to be used site wide in meta tags
if (ini_get('default_charset') != $INSTALLER09['char_set']) {
    ini_set('default_charset', $INSTALLER09['char_set']);
```

## Notes:
The French pack is still a work in progress ^^