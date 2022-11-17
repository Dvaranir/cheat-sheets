# Patches Aapanel:
## Remove PRO

## Go to 
server/panel/BT-Panel/static/js/index.js

## Go to end of the file
``` javascript
product_recommend.init(function(){
    index.get_product_status(function(){
        index.recommend_paid_version()
    });
    index.get_index_list();
})
```
## Comment/Delete `
``` javascript
index.get_product_status(function(){
	index.recommend_paid_version()
});
```
`
# Increase the number of pinned plugins
1) Go to server/panel/config/index.json
2) Delete "webssh", "safeip", "masterslave", "nginx",