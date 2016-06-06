## q-risotto

**Q**lik **R**EST **I**n **S**ense (**otto**) - a RESTful Engine API wrapper

Inspired by project [chartcacher] by [Alexander Karlsson]. 

[chartcacher]: https://github.com/mindspank/chartcacher
[Alexander Karlsson]: https://github.com/mindspank

![q-risotto](./q-risotto-logo.png)

The intention was to provide an easy access to apps, objects and its data on a Qlik Sense server thru a REST API to integrate with other systems.

The development state of this API is at the very beginning and highly incomplete, so more or less raw and unground. But see yourself.

### Endpoints

See also: [routes.js](./routes/routes.js)

/v1/**docs** - all docs on server, returns getDocList().**qDocList**

/v1/docs/**{docId}** - app layout, returns getAppLayout().**qLayout**

/v1/docs/{docId}/**objects** - all objects of app, returns getAllInfos().**qInfos**

/v1/docs/{docId}/objects/**{objId}** - object layout, returns getLayout().**qLayout**

/v1/docs/{docId}/objects/{objId}/**data** - object data, returns either getHyperCubeData()/getListObjectData().**qDataPages** depending on objectype chart/listbox

### Usage

See [config.js](./config.js) for configurations.

Start on Qlik Sense server with `npm server` or integrate into Qlik Sense ServiceDispatcher.

Navigate with browser or other tools to `https://<qlik sense server name>:1338/<endpoint>`

### Author

**Ralf Becher**

+ [irregular.bi](http://irregular.bi)
* [twitter/irregularbi](http://twitter.com/irregularbi)
* [github.com/ralfbecher](http://github.com/ralfbecher)

### License

Copyright © 2016 Ralf Becher

Released under the MIT license.

***
