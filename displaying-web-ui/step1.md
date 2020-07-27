## Start HTTP Server
`docker run -p 80:80 -d katacoda/docker-http-server`{{execute}}

## Test
`curl localhost`{{execute}}

## Switch to "Port 80" Tab

katacoda 内のタブを切り替える事により 80 番ポートにアクセス出来ます。

## Code

index.json の environment に以下の様に書く事で、
katacoda 内のタブを切り替える事により 80 番ポートにアクセス出来ます。

```
"environment": {
    "uilayout": "terminal-iframe",
    "dashboards": [{ "name": "Port 80", "port": 80 }]
  }
```

uilayout を terminal にした場合は、ブラウザの別タブで開かれる様です。

## Port Binding

アプリケーション側で Listen IP を指定する際は、127.0.0.1 では無く 0.0.0.0 を指定する必要があるようです（公式ドキュメントより）

## Document

[公式ドキュメント](https://www.katacoda.community/accessing-ports-ui.html)

[Displaying Tabs](https://katacoda.com/scenario-examples/scenarios/dashboard-tabs)

[embedding iFrames](https://katacoda.com/scenario-examples/scenarios/dashboard-tabs-iframe)
