# Migrating Custom Node.js on dotCloud to Next dotCloud


This example project demonstrates how you can easily prepare your [node-on-dotcloud](https://github.com/dotcloud/node-on-dotcloud) app for [Next dotCloud](https://next.dotcloudapp.com).

* Move `package.json` to your project root
* Read the server port from environment variables
* Create Procfile to start server
* Remove all unnecessary legacy files

You can follow all these steps in the git [history](./commits/master).

Some application may need an older nodejs or npm version. If you haven't specified yours, you can add a **engines** section to your [package.json](https://docs.npmjs.com/files/package.json):
~~~
{
    "name": "naive",
    "description": "A package using naive versioning",
    "author": "A confused individual <iam@confused.com>",
    "version": "0.0.1",
    "dependencies": {
        "redis": "0.6.7"
    },
    "engines": {
        "node": "0.10.33",
        "npm": "2.1.11"
    }
}
~~~

With these changes you should be able to deploy your existing app on Next dotcloud. More migration guides for databases and other services are available in our [dev-center](https://next.dotcloud.com/dev-center/guides#migration-guides).
