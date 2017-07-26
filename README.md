To create this app: `meteor create wrong-ddp-package-version-reproduction --release 1.4.4.1`

The problem: Meteor creates the app with incompatible package versions (ddp package & meteor package are incombpatible)

The error: 
```
I20170726-09:56:56.210(-5)? Internal exception while processing message { msg: 'connect',
I20170726-09:56:56.210(-5)?   session: 'C25WdMWFhMqtBW7BT',
I20170726-09:56:56.211(-5)?   version: '1',
I20170726-09:56:56.211(-5)?   support: [ '1', 'pre2', 'pre1' ] } Cannot read property 'get' of undefined TypeError: Cannot read property 'get' of undefined
I20170726-09:56:56.211(-5)?     at withoutInvocation (packages/meteor.js:443:33)
I20170726-09:56:56.212(-5)?     at bindAndCatch (packages/meteor.js:452:33)
I20170726-09:56:56.212(-5)?     at Object._.extend.setInterval (packages/meteor.js:479:24)
I20170726-09:56:56.213(-5)?     at [object Object]._.extend._startHeartbeatIntervalTimer (packages/ddp-common.js:89:44)
I20170726-09:56:56.213(-5)?     at [object Object]._.extend.start (packages/ddp-common.js:84:10)
I20170726-09:56:56.213(-5)?     at new Session (packages/ddp-server/livedata_server.js:318:20)
I20170726-09:56:56.213(-5)?     at [object Object]._.extend._handleConnect (packages/ddp-server/livedata_server.js:1463:29)
I20170726-09:56:56.214(-5)?     at packages/ddp-server/livedata_server.js:1379:18
```