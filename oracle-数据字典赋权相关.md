# oralce数据字典相关的权限
******************************************************

## oralce的数据库DBA角色登录和普通角色登录的区别
1. DBA角色就是SYS这样的用户，拥有大量的oralce数据字典VIEW的查看权限（类似：dba_tables、dba_objects等等）
2. 普通用户不进行赋权是无法访SYS用户拥有的数据字典表的，所以必须在**SYS管理权限下登录**,然后赋权给普通用户，才能使普通用户使用数据字典权限

 ```grant select any dictionary to scott```
 
 ```revoke select any dictionary from scott```