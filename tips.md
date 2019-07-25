+ my-shop-web-admin
	- abstracts
	- dao
	- service
	- web
		- controller
		- intercepter
+ my-shop-web-api
	- dao
	- service
	- web
		- controller
		- dto
+ my-shop-web-ui
	- api
	- constant
	- controller
	- dto
	- interceptor

首先，admin模块里，为后端业务，直接指向数据库的增删改查，及可视化crud

而api模块里，是也是有与数据库交互，但皆是查询，即权限不够

在ui模块里，是通过api模块中的requestmapping的value 在ui的controller是进行使用。也就说ui模块不与数据库进行交互，而是通过api模块调用，达到一定的分离。

通过上面的目录，可以看到dto包，这个包是用来对得到的数据进行解析，分离一定需要的数据传输对象到web中使用。

在ui模块里的api包中，在这里与api模块交互，使用一定的方法！