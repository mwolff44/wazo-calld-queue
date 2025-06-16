Add queue control to wazo-calld and publish to Wazo websocket Queue log from wazo-call-logd.

Installation
------------

    wazo-plugind-cli -c "install git https://github.com/mwolff44/wazo-calld-queue"

Configuration
-------------

Add tenant_uuid in /etc/wazo-calld/conf.d/01-queue.yml

```
calld_queue_tenant_uuid: "6209d5e0-4015-4853-ab2b-2e556bef5e46"
```

Use
---

Check the API in your wazo in calld section in http://wazo_ip/api
