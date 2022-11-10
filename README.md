# china_phone_geo_mysql
中国大陆手机号归属地mysql库

全部共**463561**条
  - 中国电信 `100931`
  - 中国移动 `225157`
  - 中国联通 `137473`

### 表结构
```mysql
CREATE TABLE `china_phone_geo` (
	`id` INT ( 11 ) NOT NULL AUTO_INCREMENT,
	`mobile` VARCHAR ( 50 ) DEFAULT NULL COMMENT '手机号码号段前7位数',
	`province` VARCHAR ( 50 ) DEFAULT NULL COMMENT '省份',
	`city` VARCHAR ( 50 ) DEFAULT NULL COMMENT '城市',
	`carrier` VARCHAR ( 50 ) DEFAULT NULL COMMENT '运营商',
	`tel_area_code` VARCHAR ( 50 ) DEFAULT NULL COMMENT '电话区号',
	`zip_code` VARCHAR ( 50 ) DEFAULT NULL COMMENT '邮编',
	`card_type` VARCHAR ( 50 ) DEFAULT NULL COMMENT '手机卡类型',
	`mobile_prefix` VARCHAR ( 50 ) DEFAULT NULL COMMENT '手机号码号段开头',
	PRIMARY KEY ( `id` ),
UNIQUE KEY `idx_mobile` ( `mobile` ) USING BTREE 
) ENGINE = MyISAM DEFAULT CHARSET = utf8mb4 COMMENT = '手机号归属地';
```
