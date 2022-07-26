# eclipse_multiCharacter
## Requirements
- [es_extended](https://github.com/zaphosting/esx_12) (you can choose any version which support multichar)

## Installation:


Go to `es_extended/config.lua` and set `Multichar`, `Identity` - true 


![image](https://user-images.githubusercontent.com/36680471/172398813-2e0d066c-424e-4399-9aa5-cee8dfa589f2.png)


Put `eclipse_multicharacter` in your resources folder.
Ensure `eclipse_multicharacter` in your server cfg.

Configure `eclipse_multicharacter/client/config.lua` and  `eclipse_multicharacter/language.json` files.

add to your database
```
CREATE TABLE `multicharacter_slots` (
	`identifier` VARCHAR(60) NOT NULL,
	`slots` INT(11) NOT NULL,
	PRIMARY KEY (`identifier`) USING BTREE,
	INDEX `slots` (`slots`) USING BTREE
) ENGINE=InnoDB;

ALTER TABLE `users` ADD COLUMN
	`disabled` TINYINT(1) NULL DEFAULT '0';
```

Ready! Start server and enjoy!

For more questions douglasprod#6686 && https://discord.gg/8nXR6rfB2C
