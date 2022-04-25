# Hbase

### Create
```
create 'notifications' 'attributes', 'metrics'
```
- notification-> column name
- attributes+metrics -> column family

### Insert
```
put 'notifications', 2,'attributes:for_user','Chaz'
```
### Update Row
```
put 'notifications' 2 , 'metrics:open',0
```

### Retrive Row
```
get 'notifications',2
```

### Retrive a range of row
```
scan 'notifcations' ,{columns=['attributes:type'],Limit=> 1,STARTROW=>2,STOPROW=>2}
```
### Delete row
```
delete 'notifications',2,'attributes:for_user'
```
### Drop table 
```
drop 'notifications'
disable 'notification' # so not to recive any error msg while drop
drop 'notifications'
```
